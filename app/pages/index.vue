<script setup lang="ts">
const { data: page } = await useAsyncData('index', () => queryCollection('landing').path('/').first())
if (!page.value) {
  throw createError({ statusCode: 404, statusMessage: 'Page not found', fatal: true })
}

const title = page.value.seo?.title || page.value.title
const description = page.value.seo?.description || page.value.description

useSeoMeta({
  titleTemplate: '',
  title,
  ogTitle: title,
  description,
  ogDescription: description,
  ogImage: '/img/assets/tfm-doctrine-home-screenshot-light.png',
  twitterImage: '/img/assets/tfm-doctrine-home-screenshot-light.png',
  ogUrl: 'https://doctrine.thefreemavens.org/',
  twitterTitle: title,
  twitterDescription: description
})
</script>

<template>
  <div>
    <AppHero />
    <AppFeaturesLearn />
    <AppFeaturesContribute />
    <AppCallAction />
  </div>
</template>
