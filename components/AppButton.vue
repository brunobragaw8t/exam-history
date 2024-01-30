<script setup lang="ts">
const props = defineProps<{
  to?: string;
  label?: string;
  icon?: string;
}>()

const componentIs = computed(() => {
  if (props.to) {
    return resolveComponent('NuxtLink')
  }

  return 'button'
})
</script>

<template>
  <component
    :is="componentIs"
    :to="to"
    class="inline-flex items-center gap-2 px-4 py-2 text-white bg-primary rounded-lg duration-150 hover:bg-primary-200 active:bg-primary-300"
  >
    <Icon v-if="icon" :name="icon" class="w-5 h-5" />
    <span v-if="label">{{ label }}</span>
  </component>
</template>
