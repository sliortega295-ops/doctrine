<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const ctaJoin = ref<ButtonProps[]>([
  {
    label: 'The Initiatory Path',
    to: '/getting-started/',
    trailingIcon: 'i-local-arrow-right',
    variant: 'solid'
  },
  {
    label: 'The Maven Code',
    to: '/getting-started/usage',
    trailingIcon: 'i-local-arrow-right',
    variant: 'subtle'
  }
])
</script>

<template>
  <UPageSection>
    <UPageCTA
      title="The Guided Path"
      description="The Maven Code is the Collective's structured curriculum that turns the Doctrine into actionable understanding. Progress in the initiatory path of Entered, Fellow, and Master Maven by applying the immutable principles of Natural Law to your life."
      :links="ctaJoin"
      spotlight
      class="shadow-md dark:bg-neutral-950"
    >
      <StarsBg />
    </UPageCTA>
  </UPageSection>
</template>
