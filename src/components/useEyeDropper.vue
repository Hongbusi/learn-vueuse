<script setup lang="ts">
const { isSupported, open, sRGBHex } = useEyeDropper()
</script>

<template>
  <p>isSupported: {{ isSupported }}</p>
  <p>sRGBHex: <span :style="{ color: sRGBHex }">{{ sRGBHex }}</span></p>
  <button :disabled="!isSupported" @click="open">
    Open Eye Dropper
  </button>
</template>
