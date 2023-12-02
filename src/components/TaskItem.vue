<script>
export default {
  props: {
    task: {
      type: Object,
    },
  },
};
</script>

<template>
  <li>{{ task.detail }}</li>
</template>

<style scoped>
li {
  padding: 0.5rem;
  font-size: 1.6rem;
  font-weight: semibold;
  color: var(--gray);
  background-color: var(--slate);
  margin-bottom: 0.5rem;
  border: solid 2px transparent;
  border-radius: 5px;
  padding: 1rem;
}

li:hover {
  color: light;
  border: solid 2px var(--green);
  cursor: pointer;
  color: var(--light);
}
</style>
