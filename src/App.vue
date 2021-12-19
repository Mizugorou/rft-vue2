<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Contain></Contain>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Contain from './components/Contain.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Contain
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
