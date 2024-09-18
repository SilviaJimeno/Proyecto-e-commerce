<template>
  <div id="app">
   <Home/>
  </div>
</template>

<script>
import Home from './components/Home.vue';

export default {
  components: {
   Home
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  display: flex;
  background-color: lightskyblue;
  justify-content: center;
  align-items: flex-start;
  height: auto;
  width: 99%;
  min-height: 100vh;
}
</style>
