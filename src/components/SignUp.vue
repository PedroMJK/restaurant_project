<template>
    <div>
        <img class="logo" src="../assets/restaurant_logo.jpg" />
        <h1>Sign Up</h1>
        <div class="register">
            <input type="text" v-model="name" placeholder="Enter with a name">
            <input type="email" v-model="email" placeholder="Enter with a email">
            <input type="password" v-model="password" placeholder="Enter with a password">
            <button v-on:click="signUp">Sign Up</button>
        </div>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "SignUp",
        data() {
            return {
                name: '',
                email: '',
                password: ''
            }
        },
        methods: {
            async signUp() {

                let result = await axios.post("http://localhost:3000/user", {
                    email: this.email,
                    password: this.password,
                    name: this.name
                });

                console.warn(result);
                if (result.status === 201) {
                    localStorage.setItem("user-info",JSON.stringify(result.data));
                    this.$router.push({ name:"HomePage"})
                }
            }
        },
        mounted() {
            let user = localStorage.getItem('user-info');

            if(user){
                this.$router.push({ name:"HomePage"})            }
        }
    }
</script>

<style>
.logo {
    width: 200px;
}
.register input {
    width: 300px;
    height: 40px;
    padding-left: 20px;
    display: block;
    margin-bottom: 30px;
    margin-right: auto;
    margin-left: auto;
    border: 1px solid skyblue;
}

.register button {
    width: 320px;
    height: 40px;
    border: 1px solid skyblue;
    background-color: skyblue;
    color: white;
    cursor: pointer;
}

</style>