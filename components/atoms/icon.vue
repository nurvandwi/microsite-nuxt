<template>
  <div class="">
    <img class="mx-auto" :src="src" />
    <p class="text-xs text-youngpurple font-bold text-center">{{ text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>