<template>
    <div>
        <h3>{{info.title}}</h3>

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