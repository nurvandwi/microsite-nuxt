<template>
  <div>
    <Home
      :user-name="'Budi Setiawan'"
      :data-table-national="dataTableNational"
      :data-table-cluster="dataTableCluster"
      :data-table-region="dataTableRegion"
      :data-table-wilayah="dataTableWilayah"
      :data-table-area="dataTableArea"
      :data-table-distributor="dataTableDistributor"
      :data-table-outlet="dataTableOutlet"
    />
  </div>
</template>

<script>
import axios from 'axios'
import Home from '../organisms/Home.vue'
export default {
  components: {
    Home,
  },

  data() {
    return {
      dataTableNational: {
        data: null,
      },
      dataTableCluster: {
        data: [],
      },
      dataTableRegion: {
        data: [],
      },
      dataTableWilayah: {
        data: [],
      },
      dataTableArea: {
        data: [],
      },
      dataTableDistributor: {
        data: [],
      },
      dataTableOutlet: {
        data: [],
      },
    }
  },
  mounted() {
    this.getdataTableNational()
    this.getdataTableCluster()
    this.getdataTableRegion()
    this.getdataTableWilayah()
    this.getdataTableArea()
    this.getdataTableDistributor()
    this.getdataTableOutlet()
  },
  methods: {
    getdataTableNational() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyODk3NzI3fQ.UXn20PC7tlp_chPDEFrDcqapMTM4hOJo4i8Mg5u_7vk',
          },
        })
        .then((res) => (this.dataTableNational = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableCluster() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/achieve`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableCluster = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableRegion() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/region`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableRegion = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableWilayah() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/hr`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableWilayah = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableArea() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/area`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableArea = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableDistributor() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/distributor`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableDistributor = res.data.data))
        .catch((err) => console.log(err))
    },
    getdataTableOutlet() {
      axios
        .get(`http://api.apolo.inosis.id/api/v1/sales/summary/outlet`, {
          headers: {
            Authorization:
              'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7InVzZXJfaWQiOiJzdXBlciIsInVzZXJfcGFzc3dvcmQiOiIqNEFDRkUzMjAyQTVGRjVDRjQ2Nzg5OEZDNThBQUIxRDYxNTAyOTQ0MSIsIm5hbWUiOm51bGwsInVzZXJfcHJvZmlsZSI6IiIsImxldmVsIjoiMSIsImVtYWlsIjpudWxsLCJzY29wZSI6bnVsbCwicGhvdG8iOm51bGwsInJlZ2lkIjpudWxsfSwiaWF0IjoxNjMyNzk0OTU2fQ.QDh3nKKdSjR9zytAh8zHk-FTw616sdhjS3Fo4-lwq4g',
          },
        })
        .then((res) => (this.dataTableOutlet = res.data.data))
        .catch((err) => console.log(err))
    },
  },
}
</script>

<style>
</style>