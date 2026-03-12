<template>
  <div class="container">

    <h1>Демонстрація v-if та v-show</h1>

    <button @click="togglePanel">
      Показати / Сховати панель
    </button>

    <h2>Панель з v-if</h2>
    <div v-if="isPanelVisible" class="panel">
      Ця панель керується директивою v-if
    </div>

    <h2>Панель з v-show</h2>
    <div v-show="isPanelVisible" class="panel">
      Ця панель керується директивою v-show
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      isPanelVisible: true
    }
  },

  methods: {
    togglePanel() {
      this.isPanelVisible = !this.isPanelVisible
    }
  }
}
</script>

<style>
.container {
  font-family: Arial;
  padding: 20px;
}

button {
  margin-bottom: 20px;
  padding: 8px 12px;
}

.panel {
  padding: 15px;
  margin-bottom: 20px;
  background: #f0f0f0;
  border: 1px solid #ccc;
}
</style>