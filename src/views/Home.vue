<template>
  <div class="home">
    <app-bar title="TODO" :left="bars" :right="search" />
    <avatar />
    <gradient />
    <todo-list />
  </div>
</template>

<script>
import Avatar from '@/components/Avatar.vue'
// @ is an alias to /src
import AppBar from "@/components/AppBar.vue"
import Gradient from '@/components/Gradient.vue'
import TodoList from '@/components/TodoList.vue';
export default {
  name: "Home",
  components: {
    AppBar,
    Avatar,
    Gradient,
    TodoList
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