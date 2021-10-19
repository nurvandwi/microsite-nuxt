<template>
  <div :class="styleBgSubtitle">
    <p :class="styleSubtitle">
      {{ subtitle }}
    </p>
  </div>
</template>

<script>
export default {
  props: ['styleBgSubtitle', 'styleSubtitle', 'subtitle'],
}
</script>

<style>
</style>