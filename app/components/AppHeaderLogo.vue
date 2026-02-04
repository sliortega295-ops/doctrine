<script setup lang="ts">
// const appConfig = useAppConfig()
const localePath = useLocalePath()
</script>

<template>
  <div class="flex">
    <NuxtLink
      :to="localePath('/')"
      aria-label="The Freemavens | Home"
      class="flex justify-center items-center"
    >
      <UIcon
        name="i-local-tfm"
        class="flex w-10 h-10"
      />
    </NuxtLink>
  </div>
</template>
