<template>
  <div class="tabbar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {

  },
};
</script>

<style scoped>
  .tabbar{
    width: 100%;
    height: 70px;
    display: flex;
    align-items: center;
    text-align: center;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .1);
  }
</style>
