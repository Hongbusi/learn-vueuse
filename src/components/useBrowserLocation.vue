<template>
  Browser Location: {{ location }}
</template>

<script setup lang="ts">
const location = useBrowserLocation()
</script>
