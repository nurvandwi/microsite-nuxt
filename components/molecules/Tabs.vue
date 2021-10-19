<template>
  <div class="mx-auto">
    <ul class="flex justify-evenly text-xs items-center my-2">
      <div v-for="(tab, index) in tabs" :key="index">
        <li
          class="cursor-pointer py-3 px-4 rounded-full transition"
          :class="
            activeTab === index
              ? 'bg-purple-900 text-white '
              : '  text-gray-500'
          "
          @click="activeTab = index"
          v-text="tab"
        ></li>
      </div>
    </ul>
    <div class="">
      <div v-show="activeTab === 0">
        <TableFourColoumn
          :title-header="'RINGKASAN PENJUALAN 10 BESAR'"
          :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
        >
          <template #thead>
            <thead>
              <tr>
                <th class="px-1 py-1" v-for="list in listTheadSale" :key="list">
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
            <tr
              v-for="data in dataTableWilayah"
              :key="data.wilayah"
              class="py-2"
            >
              <td class="px-1 py-1 text-left text-xxs">{{ data.wilayah }}</td>
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
      <div v-show="activeTab === 1">
        <TableFourColoumn
          :title-header="'RINGKASAN PENJUALAN 10 BESAR'"
          :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
        >
          <template #thead>
            <thead>
              <tr>
                <th class="px-1 py-1" v-for="list in listTheadSale" :key="list">
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
            <tr v-for="data in dataTableRegion" :key="data.region" class="py-2">
              <td class="px-1 py-1 text-left text-xxs">{{ data.region }}</td>
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
      <div v-show="activeTab === 2">
        <TableFourColoumn
          :title-header="'RINGKASAN PENJUALAN 10 BESAR'"
          :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
        >
          <template #thead>
            <thead>
              <tr>
                <th class="px-1 py-1" v-for="list in listTheadSale" :key="list">
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
            <tr v-for="data in dataTableArea" :key="data.city" class="py-2">
              <td class="px-1 py-1 text-left text-xxs">{{ data.city }}</td>
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
      <div v-show="activeTab === 3">
        <TableFourColoumn
          :title-header="'RINGKASAN PENJUALAN 10 BESAR'"
          :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
        >
          <template #thead>
            <thead>
              <tr>
                <th class="px-1 py-1" v-for="list in listTheadSale" :key="list">
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
            <tr
              v-for="data in dataTableDistributor"
              :key="data.distributor"
              class="py-2"
            >
              <td class="px-1 py-1 text-left text-xxs">
                {{ data.distributor }}
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
      <div v-show="activeTab === 4">
        <TableFourColoumn
          :title-header="'RINGKASAN PENJUALAN 10 BESAR'"
          :style-header="'px-2 py-3 bg-purple-900 border-2 rounded-t-2xl'"
        >
          <template #thead>
            <thead>
              <tr>
                <th class="px-1 py-1" v-for="list in listTheadSale" :key="list">
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
            <tr
              v-for="data in dataTableOutlet"
              :key="data.outlet_name"
              class="py-2"
            >
              <td class="px-1 py-1 text-left text-xxs">
                {{ data.outlet_name }}
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
  </div>
</template>

<script>
import TableFourColoumn from '../molecules/TableFourColoumn.vue'
export default {
  components: {
    TableFourColoumn,
  },
  props: [
    'dataTableRegion',
    'dataTableWilayah',
    'dataTableArea',
    'dataTableDistributor',
    'dataTableOutlet',
  ],

  data() {
    return {
      activeTab: 0,
      tabs: ['Wilayah', 'Region', 'Area', 'Distributor', 'Outlet'],
      listTheadSale: ['KETERANGAN', 'TARGET', 'AKTUAL', '%'],
    }
  },
  methods: {},
}
</script>

<style>
</style>