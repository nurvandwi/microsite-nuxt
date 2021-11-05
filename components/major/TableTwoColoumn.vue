<template>
  <div class="py-2 mx-auto xl:w-full">
    <div class="px-2 py-3 bg-red-600 border-2 rounded-t-2xl p-20">
      <div class="max-w-md mx-auto">
        <p class="text-center text-white font-bold">{{ title }}</p>
        <p class="text-center text-white font-bold">{{ subtitle }}</p>
      </div>
    </div>
    <div
      class="border-r-2 border-b-2 border-l-2 rounded-b-xl py-1 border-gray-300"
    >
      <div class="grid grid-cols-2">
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
      <hr class="border-red-400 mx-auto w-11/12" />
      <div class="grid grid-cols-2 py-1">
        <div>
          <p class="text-gray-400 font-bold pt-1 text-xs text-center">
            SELISIH PENJUALAN
          </p>
        </div>
        <div>
          <p class="text-gray-900 font-bold text-md text-center">
            Rp.1.987.650.000
          </p>
        </div>
      </div>
      <hr class="border-red-400 mx-auto w-11/12" />
      <div class="grid grid-cols-2 gap-1 px-1 py-2">
        <CardRounded />
      </div>
      <hr class="border-red-400 mx-auto w-11/12" />
      <ThePoin class="py-1" />
      <hr class="border-red-400 mx-auto w-11/12" />
      <nuxt-link to="/detailpenjualan">
        <ButtonDetail />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import ThePoin from '../major/ThePoin.vue'
import ButtonDetail from './ButtonDetail.vue'
import CardRounded from './CardRounded.vue'
export default {
  components: {
    CardRounded,
    ButtonDetail,
    ThePoin,
  },
  props: ['title', 'subtitle'],
}
</script>

<style>
</style>