<template>
  <h3 :class="styleTitle">{{ title }}</h3>
</template>

<script>
export default {
  props: ['title', 'styleTitle'],
}
</script>

<style>
</style>