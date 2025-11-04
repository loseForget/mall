<template>
  <div>
    <nav-bar class="navbar"><div slot="center">购物街</div></nav-bar>
    
    <scroll>
      <home-swiper :banners="banners"></home-swiper>
      <recommend :recommend="recommend"></recommend>
    </scroll>
  </div>
</template>

<script>
  import NavBar from 'components/common/navbar/NavBar.vue';
  import Scroll from 'components/common/scroll/Scroll.vue';

  import HomeSwiper from './comps/HomeSwiper.vue';
  import Recommend from './comps/Recommend.vue';

  import { getMultidata } from 'network/home';
  export default {
    data() {
      return {
        banners: [],
        recommend: []
      }
    },
    components: {
      NavBar,
      HomeSwiper,
      Scroll,
      Recommend
    },
    created() {
      this.getMultidata();
    },
    methods: {
      getMultidata() {
        getMultidata().then(res => {
          console.log(res.data)
          const data = res.data;
          this.banners = data.banner.list;
          this.recommend = data.recommend.list;
        })
      }
    },
  };
</script>

<style scoped>
  .navbar{
    background-color: var(--color-high-text);
    color: #fff;
  }
</style>
  