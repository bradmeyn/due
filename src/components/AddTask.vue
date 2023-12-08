<script setup>
import {ref} from 'vue';
import TaskModal from './TaskModal.vue'

const isModalActive = ref(false);

</script>

<template>
 <button>
    +
 </button>

 <TaskModal :isModalActive="isModalActive"  />
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

button {
    color: white;
    font-weight: bold;
    font-size: 2rem;
    border-radius:5px;
    background-color: var(--green);
    padding: 0.5rem;
    width: 50px;
    height: 50px;
    cursor: pointer;
    border: transparent 1px solid;
    outline: none;

}
</style>
