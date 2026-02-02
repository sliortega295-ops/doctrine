<!-- <script setup lang="ts">
defineProps<{
  orientation?: 'horizontal' | 'vertical'
}>()
</script> -->

<!-- :class="orientation === 'vertical' ? 'flex-col space-y-4' : 'flex-row   space-x-4'" -->
<template>
  <div
    class="grid grid-cols-2 md:grid-cols-3 items-center justify-between gap-4 mt-8"
  >
    <slot />
  </div>
</template>

<!-- <style lang="postcss">
.grid img {
  @apply ring-2 ring-primary
}
</style> -->
