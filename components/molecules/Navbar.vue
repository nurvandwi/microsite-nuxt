<template>
  <div class="bg-purple-900">
    <div class="flex py-3 px-4">
      <div class="mr-auto items-center">
        <img src="image/left_arrow.svg" alt="" srcset="" />
      </div>
      <div class="self-center mx-auto">
        <p class="text-center text-md text-white">{{ NavTitle }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['NavTitle'],
}
</script>

<style>
</style>