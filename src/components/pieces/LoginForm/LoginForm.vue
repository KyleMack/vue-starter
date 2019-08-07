<template>
<div>
    <div id="login-form">
        <label>Username</label>
        <input class="w3-input" type="text" />

        <label>Password</label>
        <input class="w3-input" type="password" />

        <button class="w3-button w3-green" v-on:click="login">Login</button>
        <button class="w3-button w3-blue" v-on:click="displayRegisterForm">New User? Register!</button>
    </div>
</div>
</template>

<script>


export default {
    components: {
         
    },
    data: function(){
        return{
        }
    },
    methods: {
        displayRegisterForm: function(){
            this.$emit('change-form', 'RegisterForm')
        },
        login: function(){
            this.$emit('login')
        }
    }
}
</script>

<style>
</style>
