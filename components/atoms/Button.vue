<template>
  <div :class="styleButton">
    <button @click="$emit('tesClick')" :class="styleTitleButton">
      <p>{{ titleButton }}</p>
    </button>
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
  methods: {},
}
</script>