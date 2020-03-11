<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld :msg="message"/> -->
    <!-- <FatherComp /> -->
    <!-- <textarea>==============================</textarea> -->
	<!-- `greet` 是在下面定义的方法名 -->
	<button v-on:click="greet">Greet</button>
	<button v-on:click="say('hi')">Say hi</button>
	<button v-on:click="say('what')">Say what</button>
	<EventTest></EventTest>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import FatherComp from './components/FatherComp.vue'
import EventTest from './components/EventTest.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    FatherComp,
	EventTest
  },
  data() {
    return {
      message: "456"
    }
  },
   methods: {
      greet: function (event) {
        // `this` 在方法里指向当前 Vue 实例
        alert('Hello ' + this.message + '!')
        // `event` 是原生 DOM 事件
        if (event) {
          alert(event.target.tagName)
        }
      },
	  say: function (msg) {
		  alert(msg)
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
