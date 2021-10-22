<template>
  <div class="mx-auto">
    <ul class="flex justify-evenly text-xs items-center my-2">
      <div v-for="(tab, index) in tabs" :key="index">
        <li
          class="cursor-pointer py-3 px-4 rounded-full transition"
          :class="
            activeTab === index
              ? 'bg-purple-900 text-white '
              : '  text-gray-500'
          "
          @click="activeTab = index"
          v-text="tab"
        ></li>
      </div>
    </ul>
    <div>
      <div v-show="activeTab === 0">
        <slot name="activeTab_0"></slot>
      </div>
      <div v-show="activeTab === 1">
        <slot name="activeTab_1"></slot>
      </div>
      <div v-show="activeTab === 2">
        <slot name="activeTab_2"></slot>
      </div>
      <div v-show="activeTab === 3">
        <slot name="activeTab_3"></slot>
      </div>
      <div v-show="activeTab === 4">
        <slot name="activeTab_4"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['tabs'],

  data() {
    return {
      activeTab: 0,
    }
  },
  methods: {
    getTab() {
      this.$emit('getTab', this.activeTab)
    },
  },
  watch: {
    activeTab: 'getTab',
  },
}
</script>

<style>
</style>