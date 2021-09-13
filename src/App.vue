<template>
  <div id="app">
    <ul>
      <a href="Test">Test (a标签)</a>
      <router-link to="Test">Test (router-link to 标签)</router-link>
    </ul>
    <ul>
      <a href="HelloWorld">HelloWorld (a标签)</a>
      <router-link to="HelloWorld">HelloWorld (router-link to 标签)</router-link>
    </ul>
    <img src="./assets/logo.png">
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
