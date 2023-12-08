<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import TaskList from "./components/TaskList.vue"; 
import AddTask from './components/AddTask.vue';
import { ref } from "vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    TaskList,
    AddTask
  },
  setup() {
    const tasks = ref([
      {
        id: 1,
        detail: "Learn Vue",
      },
      {
        id: 2,
        detail: "Learn Node-RED",
      },
    ]);

    return {
      tasks,
    };
  },
};
</script>

<template>
  <Header />
  <main>
    <div class="container">
      <h1>Tasks</h1>

      <TaskList :tasks="tasks" />
      <AddTask/>
    </div>
  </main>
  <Footer />
</template>

<style scoped>
main {
  flex-grow: 1;
  padding: 2rem;
}

main > .container {
  max-width: 600px;
  margin: 0 auto;
}

h1 {
  color: var(--light);
  font-size: 4rem;
  font-weight: bold;
  margin-bottom: 1rem;
}
</style>
