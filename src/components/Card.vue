<template>
  <div class="inset-shadow-sm inset-shadow-neutral-500 px-6 py-4 rounded-lg text-white flex flex-col gap-2 max-w-67.5 h-40 ">
    <h3 class="text-md text-green-400">{{ title }}</h3>
    <p class="text-xs mt-2 leading-4 text-gray-400">{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
};
</script>
