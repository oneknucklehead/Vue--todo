<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? `Close` : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from './Button.vue'
export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: 'hello world',
    },
    showAddTask: {
      type: Boolean,
    },
  },
  components: {
    Button,
  },
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 0 20px 0;
}
</style>
