<template>
  <div class="bg-white border-2 rounded-full py-2 grid grid-cols-5 gap-5 px-4">
    <div v-for="(icon, i) in icons" :key="i">
      <a @click="linkTo(icon.link)">
        <Icon :src="icon.src" :text="icon.name" />
      </a>
    </div>
  </div>
</template>

<script>
import listIcon from '../../data/list-icon.json'
import Icon from '../atoms/icon.vue'
export default {
  components: {
    Icon,
  },
  data() {
    return {
      icons: listIcon.list,
    }
  },
  methods: {
    linkTo(routeName) {
      this.$router.push(routeName)
    },
  },
}
</script>

<style>
</style>