<script setup lang="ts">
const appConfig = useAppConfig()

interface AppConfig {
  socials?: {
    discord?: string
    telegram?: string
  }
  github?: {
    url?: string
  }
}

const typedConfig = appConfig as AppConfig
</script>

<template>
  <div class="grid grid-cols-3 gap-2 justify-center items-center w-full">
    <UButton
      v-if="typedConfig.socials?.discord"
      icon="i-local-discord"
      size="md"
      variant="soft"
      color="neutral"
      :to="typedConfig.socials.discord"
      target="_blank"
      class="flex justify-center"
    />
    <UButton
      v-if="typedConfig.socials?.telegram"
      icon="i-local-telegram"
      size="md"
      variant="soft"
      color="neutral"
      :to="typedConfig.socials.telegram"
      target="_blank"
      class="flex justify-center"
    />
    <UButton
      v-if="typedConfig.github?.url"
      icon="i-local-github"
      size="md"
      variant="soft"
      color="neutral"
      :to="typedConfig.github.url"
      target="_blank"
      class="flex justify-center"
    />
  </div>
</template>
