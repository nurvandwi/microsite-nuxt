<template>
  <div>
    <Banner />
    <CardWithContent>
      <template #content>
        <p>
          Hai, <span class="font-bold">{{ userName }}</span>
        </p>
        <p class="text-xs lg:text-blue">
          Tekan tombol dibawah ini untuk lihat detail penjualan lainnya
        </p>
        <div class="py-3">
          <p class="bg-pink-300 px-3 py-3 rounded-full text-center text-sm">
            Periode update per tanggal :
            <span class="font-bold"> 22 januari 2021 </span>
          </p>
        </div>
        <ButtonGroup />
        <TableTwoColoumn :data-table-national="dataTableNational">
          <template #tableTitle>
            <div class="px-2 py-3 bg-red-600 border-2 rounded-t-2xl p-20">
              <div class="max-w-md mx-auto">
                <p class="text-center text-white font-bold">NASIONAL</p>
              </div>
            </div>
          </template>
          <template #buttonDetail>
            <div
              class="
                grid grid-cols-4
                mx-auto
                px-4
                border-r-2 border-l-2 border-b-2
                py-2
              "
            >
              <Paragraph
                class="col-span-3 self-center text-left"
                :style-paragraph="'text-xxs text-gray-400 font-bold'"
                :paragraph="'Tekan detail untuk lihat ringkasan penjualan'"
              />
              <Button
                :title-button="'Detail'"
                :style-button="'border-2 rounded-full py-1 bg-pink-300'"
                :style-title-button="'text-xs text-black font-bold text-center'"
              />
            </div>
          </template>
        </TableTwoColoumn>
        <TableFourColoumn :data-table-cluster="dataTableCluster">
        </TableFourColoumn>
      </template>
    </CardWithContent>
  </div>
</template>

<script>
import TableFourColoumn from '../molecules/TableFourColoumn.vue'
import Paragraph from '../atoms/Paragraph.vue'
import Button from '../atoms/Button.vue'
import TableTwoColoumn from '../molecules/TableTwoColoumn.vue'
import ButtonGroup from '../molecules/ButtonGroup.vue'
import CardWithContent from '../molecules/CardWithContent.vue'
import Banner from '../molecules/Banner.vue'
export default {
  components: {
    TableFourColoumn,
    Paragraph,
    TableTwoColoumn,
    Banner,
    CardWithContent,
    ButtonGroup,
    Button,
  },
  props: ['userName', 'dataTableNational', 'dataTableCluster'],
  methods: {},
}
</script>

<style>
</style>