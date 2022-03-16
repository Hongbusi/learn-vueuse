<template>
  <p>isSupported: {{ isSupported }}</p>
  <p>Current copied: {{ text || 'none' }}</p>
  <input v-model="source" type="text">
  <button @click="handleClickCopy(source)">
    <!-- by default, `copied` will be reset in 1.5s -->
    <span v-if="!copied">Copy</span>
    <span v-else>Copied!</span>
  </button>
</template>

<script setup lang="ts">
import { useClipboard } from '@vueuse/core'

const source = ref('Hongbusi')
const { text, copy: handleClickCopy, copied, isSupported } = useClipboard({ source })
</script>
