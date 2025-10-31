<template>
  <div class="tabbart-item" @click="ItemClick">
    <div v-if="!isActive"><slot name="icon"></slot></div>
    <div v-else><slot name="icon-active"></slot></div>
    <div :style="textColor"><slot name="title"></slot></div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        
      }
    },
    props: {
      path: String,
      activeColor: {
        type: String,
        default: "red"
      }
    },
    computed: {
      isActive(){
        // return this.$route.path.indexOf(this.path) !== -1
        return this.$route.path == this.path
      },
      textColor(){
        return this.isActive ? { color: this.activeColor } : {}
      }
    },
    methods: {
      ItemClick(){
        if(this.path != this.$route.path) this.$router.replace(this.path)
      }
    },
  };
</script>

<style scoped>
  .tabbart-item{
    flex: 1;
  }
  .tabbart-item img{
    width: 40px;
    height: 40px;
  }
</style>