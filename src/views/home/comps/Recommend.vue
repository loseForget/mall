<template>
  <div class="recommend">
    <div v-for="item in recommend" class="recommend_item">
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
.recommend {
  display: flex;
  justify-content: space-around;
  padding: 10px 0 25px;
  border-bottom: 10px solid #eee;
}

.recommend_item img {
  width: 70px;
}
</style>