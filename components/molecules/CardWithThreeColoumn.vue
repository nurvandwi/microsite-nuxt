<template>
  <div class="container py-0.5">
    <div class="flex justify-between border-2 gap-0 rounded-full shadow-sm">
      <div class="self-center">
        <img class="w-8 px-2" :src="icons" />
      </div>
      <div class="self-center">
        <p class="text-xs font-semibold text-left">{{ title }}</p>
      </div>
      <div class="bg-gray-300 rounded-full py-1 px-1">
        <p class="text-xs font-bold">{{ points }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'points', 'icons'],
  data() {
    return {}
  },
}
</script>

<style>
</style>