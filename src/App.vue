<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
 
  <div id="app">
    <HelloWorld />
    <ImageCard />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ImageCard from './components/ImageCard.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    ImageCard
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
