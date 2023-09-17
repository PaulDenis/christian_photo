<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <NavBar/>
    <Homepage/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Homepage from './components/HomePage.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Homepage,
    NavBar
  }
}
</script>

<style lang="scss">
@import './Style/common.scss';

// #app {
//   font-family: Avenir, Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
</style>
