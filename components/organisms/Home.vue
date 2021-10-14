<template>
  <div>
    <Banner />
    <CardWithContent />
  </div>
</template>

<script>
import CardWithContent from '../molecules/CardWithContent.vue'
import Banner from '../molecules/Banner.vue'
export default {
  components: {
    Banner,
    CardWithContent,
  },
}
</script>

<style>
</style>