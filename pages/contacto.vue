<template>
    <h2>Listado</h2>
    
    <UTable :rows=products :columns="columns" />
</template>

<script setup lang="ts">

import { products } from "~/server/api/productos.json";
const columns = [{
  key: 'id',
  label: 'ID'
}, {
  key: 'title',
  label: 'Título',
  sortable: true
}, {
  key: 'description',
  label: 'Descripción'
}]

</script>
