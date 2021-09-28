<template>
  <div class="">
    <div
      class="my-auto mx-auto max-h-screen h-screen bg-purple-900 xl:w-2/4 fixed"
    >
      <img
        class="mx-auto w-5/7 sm:w-1/7 xl:w-4/7"
        src="~/assets/image/Group3221.png"
        alt="logo-mvg"
      />
      <div class="text-center py-1.5">
        <p class="text-2xl italic text-yellow-300 font-normal">
          Loyalti Progam
        </p>
      </div>
      <div class="text-center bg-orange mx-auto w-60 xl:w-60 rounded-full">
        <p class="text-2xl italic text-white py-0.5 font-normal">
          Mondelez Vaganza
        </p>
      </div>
    </div>
    <div class="py-80 mx-auto xl:w-full absolute h-screen">
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
          <TableFourColoumn :title="'ACH 75% - 100%'" />
          <Heading
            :heading="'10 besar pencapaian nasional'"
            :subheading="'Pilih tombol yang akan ditampilkan '"
          />
          <div class="grid grid-cols-4 gap-1 py-1">
            <div
              class="
                border-2 border-purple-200
                py-1
                rounded-full
                self-center
                transform
                hover:scale-110
                hover:bg-pink-400
                hover:text-white
                motion-reduce:transform-none
                focus:ring-2 focus:ring-red-500
              "
            >
              <p class="text-xxs text-center font-bold">REGION</p>
            </div>
            <div
              class="
                border-2 border-purple-200
                py-1
                rounded-full
                self-center
                transform
                hover:scale-110
                hover:bg-pink-400
                hover:text-white
                motion-reduce:transform-none
                focus:ring-2 focus:ring-red-500
              "
            >
              <p class="text-xxs text-center font-bold">AREA</p>
            </div>
            <div
              class="
                border-2 border-purple-200
                py-1
                rounded-full
                self-center
                transform
                hover:scale-110
                hover:bg-pink-400
                hover:text-white
                motion-reduce:transform-none
                focus:ring-2 focus:ring-red-500
              "
            >
              <p class="text-xxs text-center font-bold">DISTRIBUTOR</p>
            </div>
            <div
              class="
                border-2 border-purple-200
                py-1
                rounded-full
                self-center
                transform
                hover:scale-110
                hover:bg-pink-400
                hover:text-white
                motion-reduce:transform-none
                focus:ring-2 focus:ring-red-500
              "
            >
              <p class="text-xxs text-center font-bold">OUTLET</p>
            </div>
          </div>

          <TableFourColoumn :title10besar="'10-Greater Jakarta'" />

          <div class="px-2 py-3 bg-purple-900 border-2 rounded-t-2xl">
            <div class="max-w-md mx-auto py-2">
              <p class="text-center text-white font-bold text-sm">
                RINGKASAN PENJUALAN PER QUARTER
              </p>
            </div>

            <table class="table-auto w-full">
              <thead>
                <tr class="">
                  <th class="px-1 py-1">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-4
                        py-2
                        text-xs
                      "
                    >
                      QUARTER
                    </p>
                  </th>
                  <th class="px-1 py-1">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-4
                        py-2
                        text-xs
                      "
                    >
                      AKTUAL
                    </p>
                  </th>
                  <th class="px-1 py-1">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-4
                        py-2
                        text-xs
                      "
                    >
                      TARGET
                    </p>
                  </th>
                  <th class="px-1 py-1">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-4
                        py-2
                        text-xs
                      "
                    >
                      %
                    </p>
                  </th>
                </tr>
              </thead>
              <tbody class="bg-white">
                <tr>
                  <td class="text-xs text-black">10-Greater Jakarta</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-right">10,11%</td>
                </tr>
                <tr>
                  <td class="text-xs text-black">10-Greater Jakarta</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-right">10,11%</td>
                </tr>
                <tr>
                  <td class="text-xs text-black">10-Greater Jakarta</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-left">Rp.137.888.999</td>
                  <td class="text-xs text-black text-right">10,11%</td>
                </tr>
                <tr>
                  <td class="text-xs text-black">Total</td>
                  <td class="text-xs text-black text-left font-bold">
                    Rp.1.137.888.999
                  </td>
                  <td class="text-xs text-black text-left px-0 font-bold">
                    Rp.1.137.888.999
                  </td>
                  <td class="text-xs text-right text-black font-bold">
                    101,11%
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
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