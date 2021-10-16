<template>
  <div class="home">
    <app-bar title="TODO" :left="bars" :right="search" />    
  </div>
</template>

<script>
// @ is an alias to /src
import AppBar from "../components/AppBar.vue"
export default {
  name: "Home",
  components: {
    AppBar
  },
};
</script>
<style lang="scss" scoped>
.home {
  height: 100%;
  width: 100%;
  overflow: hidden;
  color: white;
}
</style>