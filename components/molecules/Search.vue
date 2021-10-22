<template>
  <div class="pt-2">
    <Input @dataKeyword="keyword"> </Input>
  </div>
</template>

<script>
import Input from '../atoms/Input.vue'
export default {
  components: { Input },
  methods: {
    keyword(value) {
      this.$emit('getKeyword', value)
    },
  },
}
</script>

<style>
</style>