<template>
  <div class="navbar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
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
  .navbar{
    height: 44px;
    line-height: 44px;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    display: flex;
    box-shadow: 0 1px 1px rgba(100, 100, 100, .1);
  }

  .left, .right{
    width: 60px;
  }

  .center{
    flex: 1;
    text-align: center;
  }
</style>
  