<script setup lang="ts">
const props = defineProps<{
  id: string | number
}>()

const formattedId = String(props.id).padStart(3, '0')
const fileUrl = `/img/content/natural-law/p1/${formattedId}.webp`
</script>

<template>
  <UPageCard
    class="my-8"
    --spotlight
  >
    <div class="flex justify-between items-center">
      <!-- Icon + Image Name -->
      <div
        class="font-bold tracking-tight text-xs text-dimmed flex items-center"
      >
        <UIcon
          name="i-local-image"
          class="size-5 me-2"
        />
        {{ formattedId + '.webp' }}
      </div>
      <!-- Save Button -->
      <div class="flex gap-2">
        <UButton
          label="Save"
          variant="soft"
          color="neutral"
          size="xs"
          trailing-icon="i-local-download"
          :to="fileUrl"
          target="_blank"
        />
      </div>
    </div>

    <!-- Slide -->
    <div>
      <img
        :src="fileUrl"
        :alt="`Slide ${props.id}`"
        class="w-full rounded-lg"
      >
    </div>

    <!-- Default Slot -->
    <div class="--mt-8">
      <slot />
    </div>
  </UPageCard>
</template>
