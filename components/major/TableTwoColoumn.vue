<template>
  <div class="py-2 mx-auto xl:w-full">
    <div class="px-4 py-3 bg-red-600 border-2 rounded-t-2xl p-20">
      <div class="max-w-md mx-auto">
        <p class="text-center text-white font-bold">{{ title }}</p>
        <p class="text-center text-white font-bold">{{ subtitle }}</p>
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
    <hr class="w-11/12 border-red-400 mx-auto" />
    <div class="grid grid-cols-2 border-l-2 border-r-2 py-1">
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
    <hr class="w-11/12 border-red-400 mx-auto" />
    <div class="grid grid-cols-2 gap-1 border-r-2 border-l-2 px-1 py-2">
      <CardRounded v-show="this.$route.name == 'index'" />
      <CardRounded v-show="this.$route.name == 'index'" />
      <CardRounded v-show="this.$route.name == 'index'" />
      <CardRounded v-show="this.$route.name == 'index'" />
      <CardRounded v-show="this.$route.name == 'index' || 'DetailOutlet'" />
      <CardRounded v-show="this.$route.name == 'index' || 'DetailOutlet'" />
    </div>
    <hr class="w-11/12 border-red-400 mx-auto" />
    <ThePoin class="py-1" />
    <hr class="w-11/12 border-red-400 mx-auto" />
    <nuxt-link to="/detailpenjualan">
      <ButtonDetail v-show="this.$route.name == 'index'" />
    </nuxt-link>
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