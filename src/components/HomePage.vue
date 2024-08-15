<template>
    <div>
        <HeaderPage/>
        <h1>Hello, User. Welcome to home page hjl</h1>
    </div>
</template>

<script>
    import HeaderPage from './HeaderPage.vue';
    export default {
        name: 'HomePage',
        components: {
            HeaderPage
        },
        mounted() {
            let user = localStorage.getItem('user-info');

            if(!user){
                this.$router.push({name: 'SignUp'})
            }
        }
    }
</script>