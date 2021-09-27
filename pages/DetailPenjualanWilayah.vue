<template>
  <div class="bg-gray-100">
    <Navbar />
    <div class="py-3 px-4">
      <ButtonSelection />
      <SearchBar />
      <TableSelection />
      <TableSelection />
      <TableSelection />
      <TableSelection />
      <TableSelection />
    </div>
    <BottomNavigation />
  </div>
</template>

<script>
import BottomNavigation from '../components/major/BottomNavigation.vue'
import TableSelection from '../components/major/TableSelection.vue'
import SearchBar from '../components/minor/SearchBar.vue'
import ButtonSelection from '../components/major/ButtonSelection.vue'
import Navbar from '../components/major/Navbar.vue'
export default {
  components: {
    Navbar,
    ButtonSelection,
    SearchBar,
    TableSelection,
    BottomNavigation,
  },
}
</script>

<style>
</style>