<template>
    <div>
        <input type="text" placeholder="Inizia la ricerca..." v-model="store.textToSearch">
        <button  @click="$emit('performSearch')">Search</button>
    </div>
  </template>
  
  <script>
  import {store} from '../store'


  export default{
    name: "AppHeader",
    data(){
        return{
            store,
        };
    },
  };
  
  </script>
  
  <style lang="scss" scoped>
  </style>