<template>
  <h1>Productos</h1>
  <div class="grid md:grid-cols-6">
      <Card class="col-span-2 gap-20 m-10" v-for="product in products" :key="product.id" :="product"></Card>
  </div>
</template>

<script setup lang="ts">
import { products } from "~/server/api/productos.json";
</script>

<style scoped></style>
