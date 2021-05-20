<template>
  <div class="p-6 bg-white shadow flex justify-between mb-12">

    <BrandArea />

    <div class="menu-items text-lg flex justify-end">

      <div class="flex default-items">
        <nuxt-link class="flex-initial py-2 px-4" to="/problem">The Problem</nuxt-link>
        <nuxt-link class="flex-initial py-2 px-4" to="/contact">Contact</nuxt-link>
        <nuxt-link class="flex-initial py-2 px-4" to="/about">About</nuxt-link>
        <nuxt-link class="flex-initial py-2 px-4" to="/games">Games</nuxt-link>
      </div>

    </div>

  </div>
</template>

<style lang="postcss" scoped>
  div, a, h1, h2, h3, h4, h5 {
    font-family: 'Cabin Sketch', sans-serif;
  }
</style>
