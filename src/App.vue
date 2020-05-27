<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Plan msg="Welcome to Your Vue.js App"/>
    <!-- <list/>
    <dropdown/> -->
  </div>
</template>a

<script>
import Plan from './views/Plan.vue'
// import dropdown from './components/dropdown.vue'
// import list from './components/list.vue'

export default {
  name: 'App',
  components: {
    Plan,
    // dropdown,
    // list
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
