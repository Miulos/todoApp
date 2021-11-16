<template>
  <div class="todo" :class="{ todo_selected: selected }">
    <div class="todo_head" @click="handleClick">
      <div class="todo_icon" :style="{ color }"><i :class="['fa', 'fa-${todo.icon}']"></i></div>
      <div class="todo_menu"><i class="fa fa-ellipsis-v"></i></div>
    </div>
    <div class="todo_body">
      <p class="todo_tips">{{ todo.tasks.length }} Tasks</p>
      <h3 class="todo_title">{{ todo.name }}</h3>
      <div class="todo_progress">
        <span class="todo_progress_line">
          <i :style="{ width: progress, backgroundImage: progressColor }"></i>
        </span>
        <span :class="todo_progress_num">{{ progress }}</span>
      </div>
    </div>
  </div>
</template>

<script>
import {today, tomorrow} from '../shared'
export default {
  props: {
    todo: {
      type: Object,
      required: true
    },
    selected: {
      type: Boolean
    }
  },
  computed: {
    color () {
      return this.todo.colors[0]    // 时间08:14
    }
  }
}
</script>

<style>

</style>