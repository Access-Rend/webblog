<template>
  <div class="Articles">
    <h1>文章</h1>
    <ul>
      <li v-for="(item,index) in data" :key="index">{{ item + ' --编号：' + index }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Articles',
  data () {
    return {
      data: ['好文章', '顶级好文章', '烂文章']
    }
  }
}
</script>

<style scoped>

</style>
