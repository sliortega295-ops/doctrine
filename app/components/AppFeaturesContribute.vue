<script setup lang="ts">
import type { ButtonProps } from '@nuxt/ui'

const ctaContribute = ref<ButtonProps[]>([
  {
    label: 'Learn How To Contribute',
    to: '/getting-started/usage',
    trailingIcon: 'i-local-arrow-right',
    variant: 'solid'
  }
])
</script>

<template>
  <UPageSection
    title="Create. Contribute. Commit."
    description="This is a living, open-source project. Add your skills to help translate, clarify, and build tools that make this knowledge accessible to all."
    :links="ctaContribute"
  >
    <template #features>
      <UPageCard
        title="Translate the Doctrine"
        description="Join a translation team to make the texts available in your native language. All translations are peer-reviewed."
        variant="subtle"
        spotlight
        icon="i-local-globe"
      />
      <UPageCard
        title="Propose Clarifications"
        description="Submit pull requests to improve the clarity, flow, or accuracy of existing explanations."
        variant="subtle"
        spotlight
        icon="i-local-pencil-line"
      />
      <UPageCard
        title="Build Interactive Tools"
        description="Develop calculators, diagrams, or interactive exercises that help explain the principles (e.g., a Spiritual Currency Audit tool)."
        variant="subtle"
        spotlight
        icon="i-local-code"
      />
      <UPageCard
        title="Annotate & Discuss"
        description="Add contextual notes, historical references, or contemporary examples to specific passages via the discussion forum."
        variant="subtle"
        spotlight
        icon="i-local-message-circle-more"
      />
      <UPageCard
        title="Create Derivative Works"
        description="Write summarized guides, create video scripts, or design educational resources based on the Doctrine (licensed under the same open terms)."
        variant="subtle"
        spotlight
        icon="i-local-git-fork"
      />
      <UPageCard
        title="Review Contributions"
        description="Help maintain quality by reviewing and verifying the accuracy of translations, code, and edits submitted by others."
        variant="subtle"
        spotlight
        icon="i-local-search"
      />
    </template>
  </UPageSection>
</template>
