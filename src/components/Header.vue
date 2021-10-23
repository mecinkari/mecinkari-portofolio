<template>
  <div class="p-6 border-b-2 border-gray-200 dark:border-gray-900 text-center">
    <h1 class="text-3xl md:text-5xl font-bold dark:text-gray-100">Mecinkari</h1>
    <p
      class="
        leading-10
        font-semibold
        text-xl text-blue-500
        dark:text-yellow-400
      "
    >
      {{ leading }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["leading"],
};
</script>

<style>
</style>