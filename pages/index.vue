<template>
  <div class="index">
    <div class="flex mb-12 justify-center">
      <div class="w-1/2">A description goes here...maybe a picture of a truck stuck? Maybe more than that, but probably not too much more I just wrote all this to take up space.</div>
    </div>
    <div class="grid grid-cols-3 gap-4">
      <PresentationItem v-for="p in presentations" :presentation="p" :key="p._id" />
    </div>
  </div>
</template>

<script>

import { groq } from '@nuxtjs/sanity'

export default {
  data(){
    return {
      presentations:[]
    }
  },

  async fetch(){
    const query = groq`*[_type == "presentation" && !(_id in path('drafts.**')) ]`
    this.presentations = await this.$sanity.fetch(query)
    console.log(this.presentations)
  },
}

</script>

<style lang="postcss" scoped>

h2 {
  @apply text-gray-900 font-bold text-3xl mb-12;
}
</style>
