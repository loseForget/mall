<template>
  <div>
    <home-nav-bar></home-nav-bar>
    <banner :banners="banners"></banner>
    <recommend :recommend="recommend"></recommend>
  </div>
</template>

<script>
import HomeNavBar from './homeComponent/homeNavBar.vue';
import Banner from './homeComponent/banner.vue';
import Recommend from './homeComponent/recommend.vue';

import { getMultidata } from 'network/home.js';
export default {
  data() {
    return {
      banners: [],
      recommend: []
    }
  },
  components: {
    HomeNavBar,
    Banner,
    Recommend
  },
  created() {
    this.getMultidata()
  },
  methods: {
    getMultidata() {
      getMultidata().then(res => {
        this.banners = res.data.banner.list;
        this.recommend = res.data.recommend.list;
      })
    }
  },
};
</script>

<style scoped></style>