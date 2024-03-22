<template>
  <div v-for="task in tasks" :key="task.id">
    <TaskTask
      @toggle-reminder="$emit('toggle-reminder', task.id)"
      @delete-task="$emit('delete-task', task.id)"
      :task="task"
    />
  </div>
</template>

<script>
import TaskTask from "./Task";

export default {
  name: "TaskTasks",
  props: {
    tasks: Array,
  },
  components: {
    TaskTask,
  },
  emits: ["delete-task", "toggle-reminder"],
};
</script>
