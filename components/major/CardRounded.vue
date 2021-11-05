<template>
  <div class="container py-0.5">
    <div class="flex justify-between border-2 gap-0 rounded-full">
      <div class="self-center">
        <img
          class="w-4"
          src="https://img.icons8.com/material-outlined/24/000000/trophy.png"
        />
      </div>
      <div class="self-center">
        <p class="text-sm">{{ title }}</p>
      </div>
      <div class="bg-gray-300 rounded-full py-1 px-1">
        <p class="text-sm font-bold">{{ point }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    point: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>