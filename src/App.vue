<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <NavBar v-if="!ishome()"
    :current_page="current_page" @change_view="change_current_page"/>
    <HomePage v-if="current_page == 'home'"
    :current_page="current_page" @change_view="change_current_page"/>
    
    
    <Gallery v-if="current_page == 'gallery'"/>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/HomePage.vue'
import NavBar from './components/NavBar.vue'
import Gallery from './components/Gallery.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld
    HomePage,
    NavBar,
    Gallery,
  },
  props: {
  },
  data() {
    return {
      current_page: "home"
    }
  },
  methods: {
    change_current_page(new_page) {
      this.current_page = new_page;
      // console.log(this.current_page);
    },
    ishome() {
      return this.current_page === 'home';
      
    }
  }
}
</script>

<style lang="scss">
@import './Style/common.scss';

#app {
  height: 100vh;
  // width: 100vh;
  background-image: url("~@/assets/foto_sfondo.jpg");
  background-size: cover;
  background-position: center;
  overflow: scroll;
  // background-attachment: fixed;
//   font-family: Avenir, Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
}

</style>
