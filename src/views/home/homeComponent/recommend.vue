<template>
  <div class="recommend">
    <div v-for="item in recommend" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  props: {
    recommend: {
      type: Array,
      default: []
    }
  },
  methods: {

  },
};
</script>

<style scoped>
  .recommend{
    display: flex;
    padding: 10px 0 30px;
    border-bottom: 10px solid #eee;
  }

  .recommend-item{
    flex: 1;
    text-align: center;
  }

  .recommend-item img{
    width: 70px;
    height: 70px;
  }
</style>
