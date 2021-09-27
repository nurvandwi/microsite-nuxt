<template>
  <div class="xl:w-2/4 container mx-auto">
    <Navbar />
    <div class="py-2 px-2">
      <TableFourColoumn />
      <TableFourColoumn />
    </div>
  </div>
</template>

<script>
import TableFourColoumn from '../components/major/TableFourColoumn.vue'
import Navbar from '../components/major/Navbar.vue'
export default {
  components: {
    Navbar,
    TableFourColoumn,
  },
}
</script>

<style>
</style>