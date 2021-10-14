<template>
  <div :class="styleBgSubtitle">
    <p :class="styleSubtitle">Mondelez Vaganza</p>
  </div>
</template>

<script>
export default {
  props: {
    styleBgSubtitle: {
      type: String,
      required: true,
    },
    styleSubtitle: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>