<template>
  <div class="my-auto mx-auto max-h-screen bg-purple-900 xl:w-2/4">
    <div>
      <img
        class="mx-auto w-5/7 sm:w-1/7 xl:w-4/7"
        src="~/assets/image/Group3221.png"
        alt="logo-mvg"
      />
    </div>
    <div class="text-center py-1.5">
      <p class="text-2xl italic text-yellow-300 font-normal">Loyalti Progam</p>
    </div>
    <div class="text-center bg-orange mx-auto w-60 xl:w-60 rounded-full">
      <p class="text-2xl italic text-white py-0.5 font-normal">
        Mondelez Vaganza
      </p>
    </div>
    <div class="py-9 mx-auto xl:w-full">
      <div class="px-2 py-3 bg-gray-100 rounded-t-2xl p-20">
        <div class="max-w-md mx-auto">
          <p>Hai, <span class="font-bold">Budi Setiawan</span></p>
          <p class="text-xs lg:text-blue">
            Tekan tombol dibawah ini untuk lihat detail penjualan lainnya
          </p>
          <div class="py-3">
            <p class="bg-pink-300 px-3 py-3 rounded-full text-center text-sm">
              Periode update per tanggal :
              <span class="font-bold"> 22 januari 2021 </span>
            </p>
          </div>
          <ButtonSelection />
          <TableTwoColoumn :title="'Nasional'" />
          <TableFourColoumn />
          <Heading
            :heading="'10 besar pencapaian nasional'"
            :subheading="'Pilih tombol yang akan ditampilkan '"
          />
          <div class="grid grid-cols-4 gap-1 py-1">
            <div
              class="border-2 border-purple-200 py-1 rounded-full self-center"
            >
              <p class="text-xxs text-center font-bold">REGION</p>
            </div>
            <div
              class="border-2 border-purple-200 py-1 rounded-full self-center"
            >
              <p class="text-xxs text-center font-bold">AREA</p>
            </div>
            <div
              class="border-2 border-purple-200 py-1 rounded-full self-center"
            >
              <p class="text-xxs text-center font-bold">DISTRIBUTOR</p>
            </div>
            <div
              class="border-2 border-purple-200 py-1 rounded-full self-center"
            >
              <p class="text-xxs text-center font-bold">OUTLET</p>
            </div>
          </div>

          <TableFourColoumn />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from '../major/Heading.vue'
import TableFourColoumn from '../major/TableFourColoumn.vue'
import TableTwoColoumn from '../major/TableTwoColoumn.vue'
import ButtonSelection from '../major/ButtonSelection.vue'
export default {
  components: {
    ButtonSelection,
    TableTwoColoumn,
    TableFourColoumn,
    Heading,
  },
}
</script>