<template>
  <div class="shadow rounded-lg article-item p-4 bg-white mb-6">
    <nuxt-link :to="`presentations/${presentation.slug.current}`">{{ presentation.title }} </nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    presentation: Object
  }
}
</script>
