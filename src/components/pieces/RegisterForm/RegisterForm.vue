<template>
<div>
    <div id="register-form">
        
        <label>Username</label>
        <input class="w3-input" type="text" />

        <label>First Name</label>
        <input type="text" class="w3-input">

        <label>Last Name</label>
        <input type="text" class="w3-input">

        <label>Email</label>
        <input type="text" class="w3-input">

        <label>Password</label>
        <input class="w3-input" type="password" />

        <button class="w3-button w3-blue" v-on:click="login">Register</button>
        <button class="w3-button w3-green" v-on:click="displayLoginForm">Already have an account? Login!</button>
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
        displayLoginForm: function(){
            this.$emit('change-form', 'LoginForm')
        },
        login: function(){
            this.$emit('login')
        }
    }
}
</script>

<style>


</style>
