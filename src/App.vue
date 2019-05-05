<template>
  <div id="app">
    <aj3218></aj3218>
    <bj8196></bj8196>
    <ce1001></ce1001>
    <s125></s125>
    <crd043a class="man"></crd043a>
    <s98714 class="man"></s98714>
  </div>
</template>

<script>
import aj3218 from "./section/aj3218.vue";
import bj8196 from "./section/bj8196.vue";
import ce1001 from "./section/ce1001.vue";
import crd043a from "./section/crd043a.vue";
import s125 from "./section/s125.vue";
import s98714 from "./section/s98714.vue";

export default {
  name: "app",
  components: {
    aj3218,
    bj8196,
    ce1001,
    crd043a,
    s125,
    s98714
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
