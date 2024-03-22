<template>
  <header>
    <h1>{{ title }}</h1>
    <TaskButton
      class="btn"
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import TaskButton from "./Button";

export default {
  name: "TaskHeader",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    TaskButton,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
}
</style>
