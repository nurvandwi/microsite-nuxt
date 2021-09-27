<template>
  <div>
    <Navbar />
    <div class="px-2">
      <TableTwoColoumn :title="'WI'" :subtitle="'WEST INDONESIA'" />
      <TableFourColoumn />
      <Heading
        :heading="'10 Besar Pencapaian Nasional'"
        :subheading="'Pilih tombol yang akan ditekan untuk detail penjualan'"
      />
      <div class="grid grid-cols-4 gap-1 py-1">
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-bold">REGION</p>
        </div>
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-bold">AREA</p>
        </div>
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-bold">DISTRIBUTOR</p>
        </div>
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-bold">OUTLET</p>
        </div>
      </div>
      <TableFourColoumn />
    </div>
  </div>
</template>

<script>
import Heading from '../components/major/Heading.vue'
import TableFourColoumn from '../components/major/TableFourColoumn.vue'
import TableTwoColoumn from '../components/major/TableTwoColoumn.vue'
import Navbar from '../components/major/Navbar.vue'
export default {
  components: {
    Navbar,
    TableTwoColoumn,
    TableFourColoumn,
    Heading,
  },
}
</script>

<style>
</style>