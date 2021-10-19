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
              <nuxt-link to="/detailpenjualan">
                <Button
                  :title-button="'Detail'"
                  :style-button="'border-2 rounded-full py-1 bg-pink-300'"
                  :style-title-button="'text-xs text-black font-bold text-center'"
                />
              </nuxt-link>
            </div>
          </template>
        </TableTwoColoumn>
        <TableFourColoumn
          :title-header="'KLUSTER PERSENTASE PENCAPAIAN'"
          :style-header="'px-2 py-3 bg-red-600 border-2 rounded-t-2xl'"
          :data-table-cluster="dataTableCluster"
        >
          <template #thead>
            <thead>
              <tr class="">
                <th
                  v-for="list in listTheadCluster"
                  :key="list"
                  class="px-1 py-1"
                >
                  <p
                    class="
                      bg-purple-50
                      rounded-full
                      text-gray-400
                      px-4
                      py-2
                      text-xxs
                    "
                  >
                    {{ list }}
                  </p>
                </th>
              </tr>
            </thead>
          </template>
          <template #trow>
            <tr
              v-for="data in dataTableCluster"
              :key="data.cluster"
              class="py-2"
            >
              <td class="px-1 py-1 text-left text-xs">{{ data.cluster }}</td>
              <td class="py-1 text-left proportional-nums text-xxs">
                Rp. {{ data.aktualconvert }}
              </td>
              <td class="py-1 proportional-nums text-xxs text-left">
                Rp. {{ data.targetconvert }}
              </td>
              <td class="px-0 py-1 proportional-nums text-xxs">
                {{ data.pencapaian }}
              </td>
            </tr>
          </template>
        </TableFourColoumn>
        <Title
          class="pt-2"
          :title="'10 Besar Pencapaian Nasional'"
          :style-title="'font-bold'"
        />

        <Subtitle
          :style-subtitle="'font-normal text-sm'"
          :subtitle="'Pilih tombol yang akan ditampilkan detail penjualannya'"
        />
        <Tabs
          :data-table-region="dataTableRegion"
          :data-table-wilayah="dataTableWilayah"
          :data-table-area="dataTableArea"
          :data-table-distributor="dataTableDistributor"
          :data-table-outlet="dataTableOutlet"
        />
      </template>
    </CardWithContent>
  </div>
</template>

<script>
import Tabs from '../molecules/Tabs.vue'
import Title from '../atoms/Title.vue'
import Subtitle from '../atoms/Subtitle.vue'
import TableFourColoumn from '../molecules/TableFourColoumn.vue'
import Paragraph from '../atoms/Paragraph.vue'
import Button from '../atoms/Button.vue'
import TableTwoColoumn from '../molecules/TableTwoColoumn.vue'
import ButtonGroup from '../molecules/ButtonGroup.vue'
import CardWithContent from '../molecules/CardWithContent.vue'
import Banner from '../molecules/Banner.vue'
export default {
  components: {
    Tabs,
    Title,
    Subtitle,
    TableFourColoumn,
    Paragraph,
    TableTwoColoumn,
    Banner,
    CardWithContent,
    ButtonGroup,
    Button,
  },
  props: [
    'userName',
    'dataTableNational',
    'dataTableCluster',
    'dataTableRegion',
    'dataTableWilayah',
    'dataTableArea',
    'dataTableDistributor',
    'dataTableOutlet',
  ],
  data() {
    return {
      listTheadCluster: ['BULAN', 'TARGET', 'AKTUAL', '%'],
    }
  },
  methods: {},
}
</script>

<style>
</style>