<template>
    <div>
        <img class="logo" src="../assets/restaurant_logo.jpg" />
        <h1>Login</h1>
        <div class="login">
            <input type="email" v-model="email" placeholder="Enter with a email">
            <input type="password" v-model="password" placeholder="Enter with a password">
            <button>Login</button>
            <p>
                <router-link to="/sign-up">Sign Up</router-link>
            </p>
        </div>
    </div>
</template>

<script>
export default {
     name: 'LoginPage'
}
</script>