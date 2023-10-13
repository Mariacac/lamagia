<script setup>
import { products } from "./../database/card_database";
import MenuCard from "./MenuCard.vue";
</script>
<template>
  <div class="card-container">
    <MenuCard v-for="p in products" :product="p" />
  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  flex-wrap: wrap;

  justify-content: center;
  gap: 50px;
}
</style>
