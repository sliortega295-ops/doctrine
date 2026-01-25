<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const links = ref<ButtonProps[]>([
  {
    label: 'Read the Doctrine',
    to: '/getting-started',
    icon: 'i-local-arrow-right'
  },
  {
    label: 'View Contribution Guide',
    to: '/getting-started/usage',
    color: 'neutral',
    variant: 'subtle',
    icon: 'i-simple-icons-github'
  }
])
</script>

<template>
  <UPageHero
    :links="links"
    class="relative"
    orientation="horizontal"
  >
    <template #title>
      <h1>
        The <span class="text-primary">Doctrine</span> is Open.
      </h1>
    </template>

    <template #description>
      <p>The complete, structured, and immutable body of Natural Law knowledge. Learn, translate, and contribute to the source code of sovereignty.</p>
    </template>

    <template #top>
      <HeroBackground class="-z-50" />
    </template>

    <NuxtLink to="/getting-started">
      <UPageCard
        class="size-64 sm:size-72 md:size-80 lg:size-96 xl:size-112 aspect-square mx-auto rounded-2xl p-8 group relative"
        variant="ghost"
        spotlight
      >
        <AppSeed class="mx-auto group-hover:stroke-12 transition-all duration-6666 ease-out group-hover:duration-2000 text-primary group-hover:text-primary" />
      </UPageCard>
    </NuxtLink>
  </UPageHero>
</template>

<!-- <style lang="css" scoped>
@keyframes solSeed {
  from {
    transform: translateY(300px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 0.13;
  }
}

@keyframes solSeedReverse {
  from {
    transform: translateY(-300px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 0.23;
  }
}
/* animation: [name] [duration] [timing-function] [delay] [iteration-count] [direction] [fill-mode] [play-state]; */
.animateSolSeed {
  animation: solSeed 10s ease-in-out infinite alternate;
}

.animateSolSeedReverse {
  animation: solSeedReverse 16.2s ease-in-out infinite alternate;
}
</style> -->
