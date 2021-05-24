<template>
  <div class="presentation-wrap pb-12">
    <h2 class="py-6 font-medium text-2xl uppercase">{{ presentation.title }}</h2>
    <div class="bg-white rounded-lg shadow deck">

      <Deck :itemsrc="presentation.slidesUrl" />

      <div v-if="presentation.scratchUrl" class="mt-4 p-12 w-full" style="text-align:center">
        <iframe :src="presentation.scratchUrl" allowtransparency="true" width="100%" height="800" frameborder="0" scrolling="no" allowfullscreen></iframe>
      </div>

      <div v-if="presentation.tinkerCadUrl" class="mt-4 p-12 w-full" style="text-align:center">
        <iframe :src="presentation.tinkerCadUrl" allowtransparency="true" width="100%" height="800" frameborder="0" scrolling="no" allowfullscreen></iframe>
      </div>

    </div>
  </div>

</template>

<script>
import { groq } from '@nuxtjs/sanity'

export default {
  data(){
    return {
      presentation: {},
    }
  },

  async fetch(){
    const query = groq`*[_type == "presentation" && slug.current == "${this.$route.params.slug}"][0]`
    this.presentation = await this.$sanity.fetch(query)
  },

  methods: {
  }
}
</script>

<style lang="postcss" scoped>
h2 {
  font-family: 'Cabin Sketch', Verdana, Geneva, Tahoma, sans-serif;
}
</style>
