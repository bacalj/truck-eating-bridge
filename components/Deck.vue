<template>
  <iframe
    class="w-full rounded-t-lg"
    :src="itemsrc" height="521"
    allowfullscreen="true"
    allowtransparency="true"
    style="border:none;">
  </iframe>
</template>

<script>
export default {
  props: {
    itemsrc: String
  }
}
</script>
