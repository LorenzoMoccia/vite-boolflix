<template>
    <div>
        <AppCard v-for="movie in store.movies" :info="movie"/>
    </div>
  </template>
  
  <script>
  import AppCard from '../components/AppCard.vue'
  import {store} from '../store'

  export default{

    name: "AppMain",

    components: {
        AppCard,
    },

    data(){
        return{
            store,
        }
        
    }
  }
  
  </script>
  
  <style lang="scss" scoped>
  </style>