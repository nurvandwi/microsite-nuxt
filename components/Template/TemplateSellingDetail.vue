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
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMzMDcyNTA0fQ.C7dt8r4uYaJCaoXmi1hZpSMa3Zs2qyczWn8mvuviRR8',
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
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMzMDcyNTA0fQ.C7dt8r4uYaJCaoXmi1hZpSMa3Zs2qyczWn8mvuviRR8',
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