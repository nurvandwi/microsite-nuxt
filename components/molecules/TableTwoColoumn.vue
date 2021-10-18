<template>
  <div class="py-2 mx-auto xl:w-full">
    <slot name="tableTitle"></slot>
    <div class="grid grid-cols-2 border-r-2 border-l-2">
      <div>
        <p class="text-gray-400 font-bold text-xs text-center">
          TARGET PENJUALAN
        </p>
        <p class="text-gray-900 font-bold text-sm text-center">
          Rp.{{ dataTableNational.targetconvert }}
        </p>
      </div>
      <div>
        <p class="text-gray-400 font-bold text-xs text-center">
          AKTUAL PENJUALAN
        </p>
        <p class="text-gray-900 font-bold text-sm text-center">
          Rp.{{ dataTableNational.aktualconvert }}
        </p>
      </div>
    </div>
    <div class="grid grid-cols-2 py-2 border-r-2 border-l-2">
      <div>
        <p class="text-gray-400 font-bold pt-1 text-xs text-center">
          SELISIH PENJUALAN
        </p>
      </div>
      <div>
        <p class="text-gray-900 font-bold text-sm text-center">
          Rp.{{ dataTableNational.diffconvert }}
        </p>
      </div>
    </div>
    <div class="grid grid-cols-2 gap-1 px-1 py-2 border-r-2 border-l-2">
      <CardWithThreeColoumn
        v-for="content in contents"
        :key="content.title"
        :content="content"
        :points="getPoint(content.point)"
      />
    </div>
    <div
      class="
        grid grid-cols-3
        gap-1
        mx-auto
        text-center
        px-2
        border-r-2 border-l-2
      "
    >
      <Title
        :style-title="'text-xs text-gray-400 font-bold'"
        :title="'Poin Perolehan'"
      />
      <Title
        :style-title="'text-xs text-gray-400 font-bold'"
        :title="'Penukaran Poin '"
      />
      <Title
        :style-title="'text-xs text-gray-400 font-bold'"
        :title="'Sisa Poin'"
      />
      <Paragraph
        :style-paragraph="'text-base font-bold'"
        :paragraph="'234234'"
      />
      <Paragraph
        :style-paragraph="'text-base font-bold'"
        :paragraph="'234234'"
      />
      <Paragraph
        :style-paragraph="'text-base font-bold'"
        :paragraph="'234234'"
      />
    </div>
    <slot name="buttonDetail"></slot>
  </div>
</template>

<script>
import Paragraph from '../atoms/Paragraph.vue'
import Title from '../atoms/Title.vue'
import listContentCard from '../../data/list-content-card.json'
import CardWithThreeColoumn from '../molecules/CardWithThreeColoumn.vue'
export default {
  components: {
    CardWithThreeColoumn,
    Title,
    Paragraph,
  },
  props: {
    dataTableNational: {
      type: Object,
      default: () => {},
    },
  },
  data() {
    return {
      contents: listContentCard.list,
    }
  },
  methods: {
    getPoint(key) {
      return this.dataTableNational[key]
    },
  },
}
</script>

<style>
</style>