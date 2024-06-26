<script setup lang="ts">
import { reactive } from 'vue'

const state = reactive({
  label: 'Click me'
})
</script>

<template>
  <Story>
    <AppButton :label="state.label" />
  </Story>
</template>
