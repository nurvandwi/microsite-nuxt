<template>
  <div>
    <Navbar :nav-title="'DATA PENJUALAN PER WILAYAH'" />
    <div class="px-2">
      <Search @getKeyword="getKeyword" />
      <Tabs @getTab="getTab" url="wilayah-detail" class="" :tabs="tabs">
        <template #activeTab_0>
          <TableSellingData
            v-for="data in dataWilayah"
            :key="data.wilayah"
            :title="data.wilayah"
            :target="data.targetconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
            :selisih="data.diffconvert"
            :title_id="data.wilayah_id"
          />
        </template>
        <template #activeTab_1>
          <TableSellingData
            v-for="data in dataTableRegion"
            :key="data.region"
            :title="data.region"
            :target="data.targetconvert"
            :selisih="data.diffconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
          />
        </template>
        <template #activeTab_2>
          <TableSellingData
            v-for="data in dataTableArea"
            :key="data.city"
            :title="data.city"
            :target="data.targetconvert"
            :selisih="data.diffconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
          />
        </template>
        <template #activeTab_3>
          <TableSellingData
            v-for="data in dataTableDistributor"
            :key="data.distributor"
            :title="data.distributor"
            :target="data.targetconvert"
            :selisih="data.diffconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
          />
        </template>
        <template #activeTab_4>
          <TableSellingData
            v-for="data in dataTableOutlet"
            :key="data.outlet_name"
            :title="data.outlet_name"
            :target="data.targetconvert"
            :selisih="data.diffconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
          />
        </template>
      </Tabs>
    </div>
  </div>
</template>

<script>
import TableSellingData from '../molecules/TableSellingData.vue'
import Search from '../molecules/Search.vue'
import Tabs from '../molecules/Tabs.vue'
import Navbar from '../molecules/Navbar.vue'
export default {
  components: {
    Navbar,
    TableSellingData,
    Tabs,
    Search,
  },
  props: [
    'dataTableWilayah',
    'dataTableRegion',
    'dataTableArea',
    'dataTableDistributor',
    'dataTableOutlet',
  ],

  data() {
    return {
      tabs: ['Wilayah', 'Region', 'Area', 'Distributor', 'Outlet'],
      tabCategories: '',
      dataWilayah: [],
    }
  },

  methods: {
    getTab(value) {
      this.tabCategories = value
    },
    getKeyword(value) {
      if (+this.tabCategories === 0) {
        const data = this.dataWilayah.filter((data) => {
          return data.wilayah.toLowerCase().includes(value.toLowerCase())
        })
        this.dataWilayah = data
      }
    },
    setData() {
      this.dataWilayah = this.dataTableWilayah
    },
  },
  watch: {
    dataTableWilayah: 'setData',
  },
}
</script>

<style>
</style>