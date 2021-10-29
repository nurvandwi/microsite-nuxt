<template>
  <div>
    <Navbar :nav-title="'RINGKASAN DATA PENJUALAN'" />
    <div class="px-2">
      <TableTwoColoumn
        class="border-b-2"
        v-show="data.outlet_name != 'Total Pencapaian'"
        v-for="data in dataOutlet"
        :key="data.outlet_name"
        :poin-perolehan="data.achieveconvert"
        :poin-penukaran="data.redeemconvert"
        :sisa-poin="data.diffconvert"
      >
        <template #tableTitle>
          <div class="px-2 py-3 bg-red-600 border-2 rounded-t-2xl p-20">
            <div class="max-w-md mx-auto">
              <p class="text-center text-white font-bold">{{ params }}</p>
              <p class="text-center text-white font-bold">
                {{ data.outlet_name }}
              </p>
            </div>
          </div>
        </template>
        <template #tableContent>
          <div class="grid grid-cols-2 border-r-2 border-l-2">
            <div>
              <p class="text-gray-400 font-bold text-xs text-center">
                TARGET PENJUALAN
              </p>
              <p class="text-gray-900 font-bold text-sm text-center">
                Rp.{{ data.targetconvert }}
              </p>
            </div>
            <div>
              <p class="text-gray-400 font-bold text-xs text-center">
                AKTUAL PENJUALAN
              </p>
              <p class="text-gray-900 font-bold text-sm text-center">
                Rp. {{ data.aktualconvert }}
              </p>
            </div>
          </div>
          <div class="grid grid-cols-2 py-2 border-r-2 border-l-2">
            <div>
              <p class="text-gray-400 font-bold pt-1 text-xs text-center">
                SELISIH PENJUALAN
              </p>
            </div>
            <div>
              <p class="text-gray-900 font-bold text-sm text-center">
                Rp. {{ data.diff }}
              </p>
            </div>
          </div>
          <div class="grid grid-cols-2 gap-1 px-1 py-2 border-r-2 border-l-2">
            <CardWithThreeColoumn
              :title="'Registrasi'"
              :icons="'image/check-icon.png'"
              :points="data.regist"
            />
            <CardWithThreeColoumn
              :title="'Pencapaian'"
              :icons="'image/trophy-icon.png'"
              :points="data.percentage"
            />
          </div>
          <div
            class="grid grid-cols-2 gap-1 px-1 py-2 border-r-2 border-l-2"
          ></div>
        </template>
      </TableTwoColoumn>
      <div class="grid grid-cols-12 gap-2 py-2">
        <CardRegistrasi
          v-for="list in lists"
          :key="list.title"
          :data-title="list.title"
          :data-img="list.icon"
        ></CardRegistrasi>
      </div>

      <Title
        class="pt-2"
        :title="'Ringkasan Data Penjualan & Data Poin'"
        :style-title="'font-bold'"
      />

      <Subtitle
        :style-subtitle="'font-normal text-sm'"
        :subtitle="'Pilih tombol yang akan ditampilkan detail penjualannya'"
      />
      <Tabs url="home" :tabs="tabs">
        <template #activeTab_0>
          <TableFourColoumn
            :title-header="'RINGKASAN PENJUALAN PER QUARTER'"
            :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
          >
            <template #thead>
              <thead>
                <tr>
                  <th class="px-1 py-1" v-for="list in listThead" :key="list">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-3.5
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
              <tr v-for="data in dataQuarter" :key="data.kuartal" class="py-2">
                <td class="px-1 py-1 text-left text-xxs">{{ data.kuartal }}</td>
                <td class="py-1 text-left proportional-nums text-xxs">
                  Rp. {{ data.targetconvert }}
                </td>
                <td class="py-1 proportional-nums text-xxs text-left">
                  Rp. {{ data.aktualconvert }}
                </td>
                <td class="px-0 py-1 proportional-nums text-xxs">
                  {{ data.pencapaian }}
                </td>
              </tr>
            </template>
          </TableFourColoumn>
          <TableFourColoumn
            :title-header="'RINGKASAN PENJUALAN PER TAHUN'"
            :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
          >
            <template #thead>
              <thead>
                <tr>
                  <th class="px-1 py-1" v-for="list in listThead" :key="list">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-3.5
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
              <tr v-for="data in dataMonth" :key="data.bulan" class="py-2">
                <td class="px-1 py-1 text-left text-xxs">{{ data.bulan }}</td>
                <td class="py-1 text-left proportional-nums text-xxs">
                  Rp. {{ data.targetconvert }}
                </td>
                <td class="py-1 proportional-nums text-xxs text-left">
                  Rp. {{ data.aktualconvert }}
                </td>
                <td class="px-0 py-1 proportional-nums text-xxs">
                  {{ data.pencapaian }}
                </td>
              </tr>
            </template>
          </TableFourColoumn>
        </template>
        <template #activeTab_1>
          <TableFourColoumn
            :title-header="'RINGKASAN PENJUALAN PER QUARTER'"
            :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
          >
            <template #thead>
              <thead>
                <tr>
                  <th class="px-1 py-1" v-for="list in listThead" :key="list">
                    <p
                      class="
                        bg-purple-50
                        rounded-full
                        text-gray-400
                        px-3.5
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
              <tr class="py-2">
                <td class="px-1 py-1 text-left text-xxs">{{}}</td>
                <td class="py-1 text-left proportional-nums text-xxs">
                  Rp. {{}}
                </td>
                <td class="py-1 proportional-nums text-xxs text-left">
                  Rp. {{}}
                </td>
                <td class="px-0 py-1 proportional-nums text-xxs">{{}}</td>
              </tr>
            </template>
          </TableFourColoumn>
        </template>
      </Tabs>
    </div>
  </div>
</template>

<script>
import CardWithThreeColoumn from '../molecules/CardWithThreeColoumn.vue'
import listCardRegistrasi from '../../data/list-card-registrasi.json'
import CardRegistrasi from '../molecules/CardRegistrasi.vue'
import Title from '../atoms/Title.vue'
import Subtitle from '../atoms/Subtitle.vue'
import TableFourColoumn from '../molecules/TableFourColoumn.vue'
import Tabs from '../molecules/Tabs.vue'
import listContentCard from '../../data/list-content-card.json'
import TableTwoColoumn from '../molecules/TableTwoColoumn.vue'
import Navbar from '../molecules/Navbar.vue'
export default {
  props: ['dataOutlet', 'dataQuarter', 'dataMonth'],
  components: {
    Title,
    Subtitle,
    Navbar,
    TableTwoColoumn,
    Tabs,
    TableFourColoumn,
    CardRegistrasi,
    CardWithThreeColoumn,
  },
  data() {
    return {
      lists: listCardRegistrasi.list,
      contents: listContentCard.list3,
      listThead: ['BULAN', 'TARGET', 'AKTUAL', '%'],
      tabs: ['Penjualan', 'Point Reward'],
      params: this.$route.params.name,
    }
  },
  methods: {
    getPoint(key) {
      return this.dataOutlet[key]
    },
  },
}
</script>

<style>
</style>