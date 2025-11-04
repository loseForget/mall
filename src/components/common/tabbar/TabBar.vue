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
    height: 49px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    text-align: center;
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .1);
  }
</style>
  