<template>
  <div id="TopBar">
    <nav>
      <slot></slot>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'TopBar',
  data () {
    return {
      height: 0
    }
  },
  methods: {
    getHeight () {
      this.TopBar.height = window.innerHeight - 170 + 'px'
    },
    created () {
      window.addEventListener('resize', this.getHeight)
      this.getHeight()
    }
  }
}
</script>

<style scoped>
#TopBar {
  margin: 0 auto;
  justify-content: center;
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  box-shadow: 0 -2px 2px 2px rgba(0, 0, 0, 0.3);
}
</style>
