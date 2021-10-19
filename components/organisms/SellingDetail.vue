<template>
  <div>
    <Navbar />
    <div class="py-2 px-2">
      <TableFourColoumn
        :title-header="'RINGKASAN PENJUALAN PER QUARTER'"
        :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
      >
        <template #thead>
          <thead>
            <tr>
              <th v-for="list in listThead" :key="list" class="px-1 py-1">
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
          <tr v-for="data in dataTableQuarter" :key="data.kuartal" class="py-2">
            <td class="px-1 py-1 text-left text-xs">
              {{ data.kuartal }}
            </td>
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
              <th class="px-1 py-1" v-for="list in listTheadBulan" :key="list">
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
          <tr v-for="data in dataTableTahun" :key="data.bulan" class="py-2">
            <td class="px-1 py-1 text-left text-xs">
              {{ data.bulan }}
            </td>
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
    </div>
  </div>
</template>

<script>
import TableFourColoumn from '../molecules/TableFourColoumn.vue'
import Navbar from '../molecules/Navbar.vue'
export default {
  props: ['dataTableQuarter', 'dataTableTahun'],
  components: {
    Navbar,
    TableFourColoumn,
  },
  data() {
    return {
      listThead: ['QUARTER', 'TARGET', 'AKTUAL', '%'],
      listTheadBulan: ['BULAN', 'TARGET', 'AKTUAL', '%'],
    }
  },
}
</script>

<style>
</style>