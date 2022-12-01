<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue'
import axios from "axios";
import {store} from './store'


export default{
    components: {
    AppHeader,
    AppMain,
},

    data(){
      return{
        store,
      };
    },

    methods: {
      getDataResults(){

        axios.get('https://api.themoviedb.org/3/search/movie', {
          params: {
            api_key: "cbfe790cb37c4c944485b434561056f9",
            query: this.store.textToSearch,
            language: "it-IT"
          },
        }).then((response) => {
          this.store.movies = response.data.results;

        });
      }
    }
}

</script>

<template>
  <AppHeader @performSearch="getDataResults"/>
  <AppMain/>
  
</template>



<style lang="scss" scoped>
</style>