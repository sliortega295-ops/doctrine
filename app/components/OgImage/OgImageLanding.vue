<script lang="ts" setup>
import { computed } from 'vue'

const props = withDefaults(defineProps<{ title?: string, description?: string, headline?: string }>(), {
  title: 'title',
  description: 'description',
})

const title = computed(() => (props.title || '').slice(0, 60))
const description = computed(() => (props.description || '').slice(0, 200))
</script>

<template>
  <div class="w-full h-full flex items-center justify-center bg-neutral-900">
    <svg
      class="absolute right-0 top-0 opacity-50"
      width="629"
      height="593"
      viewBox="0 0 629 593"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    ><g filter="url(#a)"><path
      d="m628.5-578 10.834 483.578 167.264-453.859L659.827-87.387l305.569-374.957L676.925-74.079 1087.69-329.5 688.776-55.94l471.444-108.209L694.095-34.935l481.035 50.73-482.824-29.137L1130.8 190.83 683.602 6.5l348.438 335.49L668.927 22.441l220.63 430.45L649.872 32.754l68.908 478.765L628.5 36.32l-90.28 475.199 68.908-478.765L367.443 452.89l220.63-430.45-363.118 319.55L573.398 6.5l-447.2 184.33L564.694-13.342 81.874 15.795l481.031-50.73L96.784-164.15l471.44 108.21-398.91-273.562L580.075-74.079 291.604-462.344 597.173-87.387 450.402-548.281 617.666-94.422z"
      fill="#6342ff"
    /></g><defs><filter
      id="a"
      x=".874"
      y="-659"
      width="1255.25"
      height="1251.52"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB"
    ><feFlood
      flood-opacity="0"
      result="BackgroundImageFix"
    /><feBlend
      in="SourceGraphic"
      in2="BackgroundImageFix"
      result="shape"
    /><feGaussianBlur
      stdDeviation="40.5"
      result="effect1_foregroundBlur_199_94966"
    /></filter></defs></svg>

    <div class="flex flex-col justify-center p-8">
      <div class="flex justify-center mb-12 w-36 h-36 mx-auto">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="96"
          height="96"
          viewBox="0 0 24 24"
        ><rect
          rx="5.738"
          ry="5.738"
          width="24"
          height="24"
          style="fill:#6342ff;fill-opacity:1"
        /><path
          fill="#fff"
          d="M9.98 15.08h-.683V9.756l.817-.835h.818v6.646h3.36v-.485h-.684V9.723l.788-.803h.817v5.656l.964.99h2.604v-.485h-.922V9.544l-1.087-1.11h-2.614l-.818.834-.818-.834H9.848l-.819.834-.818-.834H5.699v.486h.922v6.16H5.7v.486h4.28"
        /></svg>
      </div>
      <h1
        v-if="title"
        class="flex justify-center m-0 text-5xl font-semibold mb-4 text-white"
      >
        <span>{{ title }}</span>
      </h1>
      <p
        v-if="description"
        class="text-center text-2xl text-neutral-300 leading-tight"
      >
        {{ description }}
      </p>
    </div>
  </div>
</template>
