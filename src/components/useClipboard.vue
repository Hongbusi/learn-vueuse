<template>
  <p>isSupported: {{ isSupported }}</p>
  <p>Current copied: {{ text || 'none' }}</p>
  <input v-model="source" type="text">
  <button @click="copy()">
    <!-- by default, `copied` will be reset in 1.5s -->
    <span v-if="!copied">Copy</span>
    <span v-else>Copied!</span>
  </button>
</template>

<script setup lang="ts">
const source = ref('Hongbusi')
const { text, copy, copied, isSupported } = useClipboard({ source })
</script>
