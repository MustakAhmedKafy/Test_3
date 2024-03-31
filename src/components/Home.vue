<template>
  <div>
    <div class="container">
      <h1>Welcome to Our Cafe!</h1>
      <button @click="goToMenu" class="btn btn-warning">View Menu</button>
    </div>
  </div>
</template>

<script setup>
import { useRouter } from "vue-router";

const router = useRouter();

const goToMenu = () => {
  router.push("/menu");
};
</script>

<style scoped>
.container{
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
