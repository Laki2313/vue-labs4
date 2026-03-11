<template>
  <div>
    <h2>{{ discipline }}</h2>
    <p>{{ topic }}</p>
  </div>
</template>

<script>
export default {
  props: {
    discipline: String,
    topic: String
  }
}
</script>

<style scoped>
h2 {
  color: green;
}
</style> 