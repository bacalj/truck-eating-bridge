<template>
  <div class="presentation-wrap pb-12">
    <h2 class="py-6 font-medium text-2xl uppercase">{{ presentation.title }}</h2>
    <div class="bg-white rounded-lg shadow deck">
      <Deck :itemsrc="presentation.slidesUrl" />
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
