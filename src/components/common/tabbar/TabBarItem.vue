<template>
  <div class="tabarItem" @click="itemClick">
    <div v-if="!isShow"><slot name="icon"></slot></div>
    <div v-else><slot name="icon-active"></slot></div>
    <div :style="activeColor"><slot name="title"></slot></div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  props: {
    path: {
      type: String,
      default: ''
    },
    aColor: {
      tyoe: String,
      default: '#f00'
    }
  },
  computed: {
    isShow() {
      return this.$route.path == this.path
    },
    activeColor() {
      return this.isShow ? { color: this.aColor } : {}
    }
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path)
    }
  },
};
</script>

<style scoped>
.tabarItem img{
    width: 24px;
    height: 24px;
    vertical-align: middle;
    margin-bottom: 3px;
  }
</style>
