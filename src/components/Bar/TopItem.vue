<template>
  <div class="TopItem">
    <div v-if="!active" @click="TopSelect">
      <slot name="icon"></slot>
    </div>
    <div v-else>
      <slot name="icon-active"></slot>
    </div>
    <div :style="TopColorChange()">
      <slot name="text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopItem',
  props: {
    path: String,
    color: {
      type: String,
      default: 'blue'
    }
  },
  methods: {
    TopSelect () {
      this.$router.replace(this.path)
    },
    TopColorChange () {
      return this.activate ? {color: this.color} : {}
    }
  },
  computed: {
    active () {
      return this.$route.path.indexOf(this.path) !== -1
    }
  }
}
</script>

<style scoped>
.TopBar {
  margin: 0 auto;
  height: max-content;
}

.TopBar img {
  width: available;
  height: max-content;
}

.TopBar span {
  margin: 0 auto;
  justify-content: center;
  display: flex;
}
</style>
