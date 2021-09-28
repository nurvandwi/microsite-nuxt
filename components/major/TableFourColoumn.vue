<template>
  <div class="">
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
        <tr class="py-2">
          <td class="px-1 py-1 text-xs">{{ title }} {{ title10besar }}</td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-0 py-1 proportional-nums text-xs">11,11 %</td>
        </tr>

        <tr class="py-2">
          <td class="px-1 py-1 text-xs">{{ title }} {{ title10besar }}</td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-0 proportional-nums text-xs">11,11 %</td>
        </tr>
        <tr class="py-2">
          <td class="px-1 py-1 text-xs">{{ title }} {{ title10besar }}</td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 137.678.111
          </td>
          <td class="px-0 proportional-nums text-xs">11,11 %</td>
        </tr>
        <tr class="py-2">
          <td class="px-1 py-1 text-xs">{{ title }} {{ title10besar }}</td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 937.678.111
          </td>
          <td class="px-1 py-1 proportional-nums text-xs text-center">
            Rp. 937.678.111
          </td>
          <td class="px-0 proportional-nums text-xs">11,11 %</td>
        </tr>
        <tr class="">
          <td class="px-1 py-1 text-xs font-bold">TOTAL</td>
          <td class="px-0 pixel:pl-3 proportional-nums text-xs font-bold">
            Rp. 1.937.678.111
          </td>
          <td class="px-0 proportional-nums text-xs font-bold pixel:pl-3">
            Rp. 1.137.678.111
          </td>
          <td class="px-0 text-xs proportional-nums font-bold">111,11%</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  props: ['title', 'title10besar'],
}
</script>

<style>
</style>