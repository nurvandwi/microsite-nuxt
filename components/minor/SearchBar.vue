<template>
  <div class="py-3">
    <div class="flex items-center border rounded-md max-w-md mx-auto bg-white">
      <div class="w-full">
        <input
          type="search"
          class="w-full px-4 py-1 text-gray-900 rounded-full focus:outline-none"
          placeholder="search"
          x-model="search"
        />
      </div>
      <div>
        <button
          type="submit"
          class="
            flex
            items-center
            justify-center
            w-12
            h-8
            text-gray-100
            bg-gray-500
            rounded-md
          "
        >
          <svg
            class="w-5 h-5"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
            ></path>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>