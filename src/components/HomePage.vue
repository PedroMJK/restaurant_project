<template>
    <div>
         <h1>Hello, User. Welcome to home page hjl</h1>
    </div>
</template>

<script>
    export default {
        name: 'HomePage',
        mounted() {
            let user = localStorage.getItem('user-info');

            if(!user){
                this.$router.push({name: 'SignUp'})
            }
        }
    }
</script>