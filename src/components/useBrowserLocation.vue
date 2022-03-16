<template>
  Browser Location: {{ location }}
</template>

<script setup lang="ts">
import { useBrowserLocation } from '@vueuse/core'

const location = useBrowserLocation()
</script>
