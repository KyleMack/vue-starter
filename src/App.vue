<template>
<div>
    <div id="content" class="w3-container">
        <div :is="currentPage" @page-changed="changePage" ></div>
    </div>
</div>
</template>

<script>

import LandingPage from './components/pages/LandingPage/LandingPage.vue'
import HomePage from './components/pages/HomePage/HomePage.vue'


export default {
    components: {
         LandingPage, HomePage
    },
    data: function(){
        return{
            currentPage: 'LandingPage'
        }
    },
    methods: {
        changePage: function(page){
            this.currentPage = page
        }
    }
}
</script>

<style>
</style>
