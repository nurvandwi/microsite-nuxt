<template>
  <div>
    <Navbar />
    <div class="px-2">
      <TableTwoColoumn
        :title="'100000-ANA047'"
        :subtitle="'JAYA MAKMUR INDAH'"
      />
      <div class="grid grid-cols-2 gap-2">
        <TheCard />
        <TheCard />
        <TheCard />
        <TheCard />
      </div>
      <Heading
        class="py-2"
        :heading="'Ringkasan data penjualan & data poin'"
        :subheading="'Pilih tombol yang akan ditampilkan penjualannya'"
      />
      <div class="grid grid-cols-4 gap-1 py-1">
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-semibold">PENJUALAN</p>
        </div>
        <div class="border-2 border-purple-200 py-1 rounded-full self-center">
          <p class="text-xxs text-center font-semibold">POIN REWARD</p>
        </div>
      </div>
      <TableFourColoumn />
      <TableFourColoumn />
    </div>
  </div>
</template>

<script>
import TableFourColoumn from '../components/major/TableFourColoumn.vue'
import Heading from '../components/major/Heading.vue'
import TheCard from '../components/major/TheCard.vue'
import TableTwoColoumn from '../components/major/TableTwoColoumn.vue'
import Navbar from '../components/major/Navbar.vue'
export default {
  components: {
    Navbar,
    TableTwoColoumn,
    TheCard,
    Heading,
    TableFourColoumn,
  },
}
</script>

<style>
</style>