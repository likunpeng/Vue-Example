<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld :msg="message"/> -->
    <FatherComp />
    <textarea>==============================</textarea>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import FatherComp from './components/FatherComp.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    FatherComp
  },
  data() {
    return {
      message: "456"
    }
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
