<template>
  <div class="bg-purple-900">
    <div class="flex py-3 px-4">
      <div class="mr-auto items-center">
        <img src="image/left_arrow.svg" alt="" srcset="" />
      </div>
      <div class="self-center mx-auto">
        <Paragraph
          :paragraph="'RINGKASAN DATA PENJUALAN'"
          :styleParagraph="'text-center text-md text-white'"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Paragraph from '../atoms/Paragraph.vue'
export default {
  components: {
    Paragraph,
  },
}
</script>

<style>
</style>