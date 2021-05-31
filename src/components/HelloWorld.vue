<template>
  <h1 :style="h1styles">HMR doesn't take effect - {{ msg }}</h1>
  <h1 :style="{ fontSize: `${fontSize}px` }">HMR take effect - {{ msg }}</h1>
</template>

<script setup>
import { defineProps, ref } from 'vue'

const props = defineProps({
  fontSize: String,
  msg: String
})

const h1styles = ref({
  fontSize: `${props.fontSize}px`
})
</script>