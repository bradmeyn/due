<script>
export default {
  name: "Header",
};
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/logo.svg" alt="" />
        <span>Due</span>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  padding: 1rem;
  background: var(--dark);
}

.logo {
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 5px;
}

img {
  height: 30px;
}

span {
  font-weight: bold;
  font-size: 1.5rem;
  color: var(--light);
}
</style>
