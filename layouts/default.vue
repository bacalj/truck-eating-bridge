<template>
  <div class="min-h-screen">
    <Navbar />
    <div class="max-w-7xl mx-auto px-8">
      <Nuxt />
    </div>
  </div>
</template>

<script>
export default {
  mounted(){
    console.log('Hi, Jules.')
  }
}
</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

a:hover {
  @apply text-indigo-500;
}
</style>
