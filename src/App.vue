<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style>
  #app {
    font-family: cursive;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #333;
    margin-top: 0;
  }
  body{
    max-width: 750px;
    margin: 0 auto;
  }
 .swiper-pagination-bullet{
    width: 18px;
    height: 18px;
  }
  .swiper-pagination-bullet-active{
    background: #f9fbfd;
  }
</style>
