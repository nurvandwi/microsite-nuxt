<template>
  <div class="mx-auto xl:w-full py-1">
    <div class="px-4 py-3 bg-purple-900 border-2 rounded-t-2xl p-20">
      <div class="max-w-md mx-auto">
        <p class="text-center text-white font-bold">WI</p>
        <p class="text-center text-white font-bold">WEST INDONESIA</p>
      </div>
    </div>
    <div class="grid grid-cols-2 border-r-2 border-l-2 py-1">
      <div>
        <p class="text-gray-400 font-bold text-xs text-center">
          TARGET PENJUALAN
        </p>
        <p class="text-gray-900 font-bold text-md text-center">
          Rp.1.987.650.000
        </p>
      </div>

      <div>
        <p class="text-gray-400 font-bold text-xs text-center">
          AKTUAL PENJUALAN
        </p>
        <p class="text-gray-900 font-bold text-md text-center">
          Rp.1.987.650.000
        </p>
      </div>
    </div>
    <div class="grid grid-cols-2 border-l-2 border-r-2 py-1">
      <div>
        <p class="text-gray-400 font-bold pt-1 text-xs text-center">
          SELISIH PENJUALAN
        </p>
        <p class="text-gray-900 font-bold text-md text-center">
          Rp.1.987.650.000
        </p>
      </div>
      <div class="self-center">
        <CardRounded />
      </div>
    </div>
    <nuxt-link to="/detailperwilayah">
      <ButtonDetail />
    </nuxt-link>
  </div>
</template>

<script>
import ButtonDetail from '../major/ButtonDetail.vue'
import CardRounded from '../major/CardRounded.vue'
export default {
  components: {
    CardRounded,
    ButtonDetail,
  },
}
</script>

<style>
</style>