<template>
  <div id="app">
    <Navbar/>
    <MainMenu/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import MainMenu from './components/MainMenu.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    MainMenu
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 100%;
  /* -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
