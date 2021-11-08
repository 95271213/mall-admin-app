<template>
  <div class="home">
    <LeftMenu />
    <div :class="{ 'main-app': true, 'menu-unfold': $store.state.collapsed }">
      <SliderNav />
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import LeftMenu from "./components/menu.vue";
import SliderNav from "./components/sliderNav.vue";
export default {
  components: {
    LeftMenu,
    SliderNav,
  },
  data() {
    return {
      collapsed: false,
    };
  },
};
</script>


<style scoped lang="less">
@import url("~@/assets/css/home.less");
</style>
