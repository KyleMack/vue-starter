<template>
<div class="w3-row">
    <div class="w3-col l4 s0"></div>
    <div id="login-form" class="w3-col l4 s12">
        <h1 class="w3-orange">DND Assistant</h1>
        <div :is="currentForm" @change-form="changeForm" @login="login" ></div>
    </div>
</div>
</template>

<script>

import LoginForm from '../../pieces/LoginForm/LoginForm.vue'
import RegisterForm from '../../pieces/RegisterForm/RegisterForm.vue'

export default {
    components: {
         LoginForm, RegisterForm
    },
    data: function(){
        return{
            currentForm: 'LoginForm'
        }
    },
    methods: {
        changeForm: function(page){
            this.currentForm = page
        },
        login: function(){
            this.$emit('page-changed', 'HomePage')
        }
    }
}
</script>

<style>

.w3-row{
    margin-top: 7%;
}
.w3-row h1{
    text-align: center;
}

#login-form h1{
    border-radius: 10px 10px 0px 0px;
}
#login-form input{
    padding: 5px 0px;
}
#login-form input:hover{
    background-color: lightgrey;
}
 
button{
    width: 100%;
}

</style>
