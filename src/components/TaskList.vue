<script>
import TaskItem from "./TaskItem.vue"; // Import the TaskItem component

export default {
  components: {
    TaskItem, // Register the TaskItem component
  },
  props: {
    tasks: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<template>
  <ul>
    <TaskItem v-for="task in tasks" :key="task.id" :task="task" />
  </ul>
</template>

<style>
ul {
  list-style: none;
}
</style>
