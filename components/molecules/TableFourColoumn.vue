<template>
  <div class="py-1">
    <div class="px-2 py-3 bg-purple-900 border-2 rounded-t-2xl">
      <div class="max-w-md mx-auto py-2">
        <p class="text-center text-white font-bold text-sm">
          RINGKASAN PENJUALAN PER QUARTER
        </p>
      </div>

      <table class="w-full text-gray-800">
        <thead>
          <tr class="">
            <th class="px-1 py-1">
              <p
                class="
                  bg-purple-50
                  rounded-full
                  text-gray-400
                  px-4
                  py-2
                  text-xs
                "
              >
                QUARTER
              </p>
            </th>
            <th class="px-1 py-1">
              <p
                class="
                  bg-purple-50
                  rounded-full
                  text-gray-400
                  px-4
                  py-2
                  text-xs
                "
              >
                AKTUAL
              </p>
            </th>
            <th class="px-1 py-1">
              <p
                class="
                  bg-purple-50
                  rounded-full
                  text-gray-400
                  px-4
                  py-2
                  text-xs
                "
              >
                TARGET
              </p>
            </th>
            <th class="px-1 py-1">
              <p
                class="
                  bg-purple-50
                  rounded-full
                  text-gray-400
                  px-4
                  py-2
                  text-xs
                "
              >
                %
              </p>
            </th>
          </tr>
        </thead>
      </table>
    </div>
    <table
      class="
        table-auto
        w-full
        mx-auto
        text-gray-800
        border-b-2 border-r-2 border-l-2 border-gray-300
      "
    >
      <tr v-for="data in dataTableCluster" :key="data" class="py-2">
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
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  props: ['dataTableCluster'],
}
</script>

<style>
</style>