<template>
  <div>
    <div class="container">
      <h2>Menu Item</h2>
     <ul class="list-group">
      <li v-for="item in menuItems" :key="item.id" class="list-group-item">
        <button @click="showAlert(item.name)" class="btn btn-success w-100">{{ item.name }}</button>
      </li>
    </ul>
    </div>
  </div>
</template>

<script setup>
const menuItems = [
  { id: 1, name: "Coffee" },
  { id: 2, name: "Tea" },
  { id: 3, name: "Sandwich" },
  { id: 4, name: "Cake" },
];

const showAlert = (itemName) => {
  alert(`You selected ${itemName}`);
};
</script>

<style scoped>
.container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
