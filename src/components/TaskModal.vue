<script setup>
const props = defineProps({
  isModalActive: Boolean,
});
</script>

<template>
  <div class="modal__container">
    <div class="modal">
      <header>
        <h2>New Task</h2>
        <button class="modal__close-btn" @click="closeModal">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            height="16"
            width="12"
            viewBox="0 0 384 512"
          >
            <path
              fill="#fff"
              d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"
            />
          </svg>
        </button>
      </header>
      <form @submit.prevent="handleSubmit">
        <label for="detail">Description</label>
        <input type="text" class="task-detail" name="detail" />
        <button type="submit" class="modal__save-btn">Save</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

h2 {
  font-size: 2rem;
  color: #fff;
  font-weight: semibold;
}

.modal__container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal {
  min-width: 20rem;
  padding: 1rem;
  background-color: var(--dark);
  border-radius: 5px;
}

.modal__close-btn {
  color: #fff;
  background-color: transparent;
  border: none;
  cursor: pointer;
  outline: none;
  padding: 0;
}

label {
  font-size: 0.8rem;
  display: block;
  margin-bottom: 0.2rem;
  color: slategray;
  font-weight: semibold;
}

input {
  display: block;
  width: 100%;
  padding: 0.5rem;
  border-radius: 5px;
  border: 0.5px solid slategray;
  margin-bottom: 1rem;
  background-color: var(--dark);
}

input:focus {
  outline: none;
  border: 0.5px solid var(--green);
}

.modal__save-btn {
  display: block;
  border-radius: 5px;
  text-align: center;
  padding: 0.5rem;
  font-size: 1.2rem;
  background-color: var(--green);
  color: white;
  width: 100%;
  font-weight: bold;
  border: none;
  cursor: pointer;
}

h2 {
  color: var(--light);
}
</style>
