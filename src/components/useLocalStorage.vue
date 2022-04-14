<script setup lang="ts">
const name = useLocalStorage('name', 'Hongbusi')
</script>

<template>
  <input v-model="name" type="text">
  <p>name: {{ name }}</p>
</template>
