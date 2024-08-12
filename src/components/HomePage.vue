<template>
    <div>
         <h1>Hello, Use. Welcome to home page</h1>
    </div>
</template>

<script>
    export default {
        name: 'HomePage',
        mounted() {
            let user = localStorage.getItem('user-info');

            if(user){
                this.$router.push({name: 'Home'})
            }
        }
    }
</script>