<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Something</h2>
  </div>
</template>

<script>
import Test from './Test'
export default {
  name: 'HelloWorld',
  components: {Test},
  data () {
    return {
      msg: 'Home Page(cpnt: HelloWorld.vue)'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
