<template>
  <div class="bg-purple-900">
    <div class="flex py-3 px-4">
      <a @click="to" class="mr-auto self-center">
        <img class="w-8" src="image/left_arrow.svg" alt="" srcset="" />
      </a>
      <div class="self-center mx-auto">
        <p class="text-center text-md text-white">{{ NavTitle }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['NavTitle'],
  methods: {
    to() {
      this.$router.go(-1)
    },
  },
}
</script>

<style>
</style>