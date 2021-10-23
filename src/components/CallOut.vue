<template>
  <p
    class="
      italic
      py-3
      px-6
      font-semibold
      text-lg
      font-mono
      rounded
      text-blue-900
      transition
      duration-200
      border
      dark:bg-opacity-5 dark:text-gray-50
    "
  >
    {{ text }}
  </p>
</template>

<script>
export default {
  name: "CallOut",
  props: ["text", "icon"],
};
</script>

<style>
</style>