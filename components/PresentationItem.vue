<template>
  <div class="shadow rounded-lg article-item bg-white mb-6">
    <div class="image-wrap h-56 flex items-center overflow-hidden justify-center">
        <SanityImage auto="format" :asset-id="presentation.poster.asset._ref" />
    </div>
    <div class="p-4 text-xl">
      <nuxt-link :to="`presentations/${presentation.slug.current}`">{{ presentation.title }} </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    presentation: Object
  }
}
</script>

<style lang="postcss" scoped>
a {
  font-family: 'Cabin Sketch'
}

a:hover {
  @apply text-indigo-500;
}
</style>
