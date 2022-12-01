<template>
    <div>
        <h3>{{info.title}}</h3>
        <p>{{info.original_title}}</p>
        <p>{{info.original_language}}</p>
        <p>{{info.vote_average}}</p>
    </div>
  </template>
  
  <script>
  
  export default{
    name: "AppCard",
    props: {
        info: Object,
    }
  }
  
  </script>
  
  <style lang="scss" scoped>
  </style>