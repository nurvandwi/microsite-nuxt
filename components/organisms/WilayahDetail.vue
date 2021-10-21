<template>
  <div>
    <Navbar :nav-title="'DATA PENJUALAN PER WILAYAH'" />
    <div class="px-2">
      <Search />
      <Tabs url="wilayah-detail" class="py-1" :tabs="tabs">
        <template #activeTab_0>
          <TableSellingData
            v-for="data in dataTableWilayah"
            :key="data.wilayah"
            :title="data.wilayah"
            :target="data.targetconvert"
            :aktual="data.aktualconvert"
            :pencapaian="data.pencapaian"
          />
        </template>
        <template #activeTab_1>
          <TableSellingData
            v-for="data in dataTableRegion"
            :key="data.region"
            :title="data.region"
            :target="data.targetconvert"
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
    }
  },
  methods: {},
}
</script>

<style>
</style>