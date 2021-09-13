<template>
  <div id="app">
    <TopBar>
      <TopItem v-for="item in TopList" :path="item.path" :color="item.color" :key="item.path">
        <img slot="icon" :src="item.image" alt="">
        <img slot="icon-active" :src="item.image_active" alt="">
        <span slot="text">{{ item.text }}</span>
      </TopItem>
    </TopBar>
    <router-view></router-view>
    <img src="./assets/logo.png">
  </div>
</template>

<script>

import TopBar from './components/Bar/TopBar'
import TopItem from './components/Bar/TopItem'

export default {
  name: 'App',
  components: {
    TopItem, TopBar
  },
  data () {
    return {
      TopList: [
        {
          path: '/articles',
          color: 'red',
          image: require('./assets/img/topbar/articles.png'),
          image_active: require('./assets/img/topbar/articles_active.png'),
          text: '文章'
        }
      ]
    }
  }
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
