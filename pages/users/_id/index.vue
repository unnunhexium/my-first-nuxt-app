<template>
  <section class="container">
    <div>A single user with ID: {{ $route.params.id }}</div>
  </section>
</template>

<script>
export default {
  validate(data) {
    return /^\d+/.test(data.params.id)
  },
  layout: 'users',
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
