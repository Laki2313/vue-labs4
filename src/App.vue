<template>
  <div class="container">
    <h1>Динамічний рендеринг станів сторінки</h1>

    <div class="buttons">
      <button @click="toggleLoading">Toggle loading</button>
      <button @click="toggleError">Toggle error</button>
      <button @click="clearItems">Clear items</button>
      <button @click="addItems">Add sample items</button>
    </div>

    <div v-if="isLoading">
      <p>Завантаження...</p>
    </div>

    <div v-else-if="hasError">
      <p>Помилка завантаження</p>
    </div>

    <div v-else-if="items.length === 0">
      <p>Немає даних</p>
    </div>

    <div v-else>
      <ul>
        <li v-for="item in items" :key="item">
          {{ item }}
        </li>
      </ul>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      isLoading: false,
      hasError: false,
      items: []
    }
  },

  methods: {
    toggleLoading() {
      this.isLoading = !this.isLoading
    },

    toggleError() {
      this.hasError = !this.hasError
    },

    clearItems() {
      this.items = []
    },

    addItems() {
      this.items = ["Елемент 1", "Елемент 2", "Елемент 3"]
    }
  }
}
</script>

<style>
.container {
  font-family: Arial;
  padding: 20px;
}

.buttons button {
  margin: 5px;
}
</style>