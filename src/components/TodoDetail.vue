<template>
  <transition name="show" @enter="handleEnter" @leaver="handleLeave">
      <div class="todo-detail" v-if="sl=elected">
          <app-bar @left="unselectTodo" />
          <todo :todo="selected.todo" />
      </div>
  </transition>
</template>

<script>
import { mapState, mapMutations } from 'vuex'
import AppBar from './AppBar.vue'
import Todo from './Todo.vue'
export default {
  components: { AppBar, Todo },
  computed: {
    ...mapState(['selected', 'unselect'])
  },
  methods: {
    ...mapMutations(['unselectedTod']),
    handleEnter (el) {
      Object.assign(el.style, {
        top: '${this.selected.rect.top}px',
        // 12:47
      })
    }
  }
}
</script>

<style lang="scss" scoped>

</style>