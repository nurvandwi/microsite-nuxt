<template>
  <SellingDetail
    :data-table-quarter="dataTableQuarter"
    :data-table-tahun="dataTableTahun"
  />
</template>

<script>
import axios from 'axios'
import SellingDetail from '../organisms/SellingDetail.vue'
export default {
  components: {
    SellingDetail,
  },
  data() {
    return {
      dataTableQuarter: {
        data: [],
      },
      dataTableTahun: {
        data: [],
      },
    }
  },
  mounted() {
    this.getdataTableQuarter()
    this.getdataTableTahun()
  },
  methods: {
    getdataTableQuarter() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/sem`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyODk3NzI3fQ.UXn20PC7tlp_chPDEFrDcqapMTM4hOJo4i8Mg5u_7vk',
          },
        })
        .then((res) => (this.dataTableQuarter = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableTahun() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/quarter`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyODk3NzI3fQ.UXn20PC7tlp_chPDEFrDcqapMTM4hOJo4i8Mg5u_7vk',
          },
        })
        .then((res) => (this.dataTableTahun = res.data.data))
        .catch((err) => console.log(err))
    },
  },
}
</script>

<style>
</style>