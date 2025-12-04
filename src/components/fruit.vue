<template>
  <div class="fruit-container">
    <h1 class="page-title">Fruit Information List</h1>

    <div class="fruit-list">
      <div v-for="fruit in list" :key="fruit.id" class="fruit-item">
        <h3 class="fruit-name">{{ fruit.name }}</h3>
        <p class="fruit-type">Color: {{ fruit.color }}</p>
        <p class="fruit-type">Price: {{ fruit.price }} $</p>
        <p class="fruit-brief">{{ fruit.info }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const list = ref([
  {
    id: 1,
    name: "Apple",
    color: "Red",
    price: 3,
    info: "Apples are nutritious fruits rich in fiber and vitamin C.",
  },
  {
    id: 2,
    name: "Banana",
    color: "Yellow",
    price: 1,
    info: "Bananas are sweet fruits high in potassium.",
  },
  {
    id: 3,
    name: "Grapes",
    color: "Purple",
    price: 2,
    info: "Grapes grow in clusters and are used to make wine and juice.",
  },
  {
    id: 4,
    name: "Orange",
    color: "Orange",
    price: 2.5,
    info: "Oranges are citrus fruits rich in vitamin C.",
  },
  {
    id: 5,
    name: "Strawberry",
    color: "Red",
    price: 4,
    info: "Strawberries are antioxidant-rich sweet red fruits.",
  },
]);
</script>

<style scoped>
.fruit-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  font-family: "Microsoft YaHei", sans-serif;
  color: #333;
}

.page-title {
  text-align: center;
  color: #2c3e50;
}

.fruit-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.fruit-item {
  background-color: #f8f9fa;
  border: 1px solid #e9ecef;
  border-radius: 8px;
  padding: 15px;
  transition: all 0.2s ease-in-out;
}

.fruit-item:hover {
  border-color: #adb5bd;
  background-color: #e9ecef;
}

.fruit-name {
  color: #2c3e50;
  margin-top: 0;
}

.fruit-type {
  color: #6c757d;
  font-size: 0.9em;
}

.fruit-brief {
  color: #495057;
}
</style>
