<template>
  <div id="app">
    <BaseNavigation />
    <router-view :key="$route.path" />
  </div>
</template>
<script>
import BaseNavigation from "@/components/BaseNavigation";

export default {
  components: {
    BaseNavigation,
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
