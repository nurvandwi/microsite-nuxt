<template>
  <div>
    <h1 class="font-bold">{{ heading }}</h1>
    <p class="font-normal text-sm">
      {{ subheading }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    heading: {
      type: String,
      required: true,
    },
    subheading: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>