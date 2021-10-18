<template>
  <div :class="styleButton">
    <a :class="styleTitleButton">
      <p>{{ titleButton }}</p>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    titleButton: {
      type: String,
      required: true,
    },
    styleButton: {
      type: String,
      required: true,
    },
    styleTitleButton: {
      type: String,
      required: true,
    },
  },
}
</script>