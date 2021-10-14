<template>
  <h3 :class="styleTitle">{{ title }}</h3>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    styleTitle: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>