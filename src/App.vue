<template>
  <div id="app">
    <TheNavigation />
    <router-view></router-view>
  </div>
</template>
<script>
import TheNavigation from "@/components/TheNavigation";
export default {
  name: "App",
  components: {
    TheNavigation,
  },
};
</script>
<style lang="scss">
@import "assets/css/main.scss";
</style>