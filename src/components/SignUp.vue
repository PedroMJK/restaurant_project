<template>
    <div>
        <img class="logo" src="../assets/restaurant_logo.jpg" />
        <h1>Sign Up</h1>
        <div class="register">
            <input type="text" placeholder="Enter With a Name" id="">
            <input type="email" placeholder="Enter With a Email" id="">
            <input type="password" placeholder="Enter With a Password" id="">
            <button>Sign Up</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SignUp"
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