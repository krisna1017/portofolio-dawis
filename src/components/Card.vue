<template>
  <div class="bg-black/50 px-6 py-4 rounded-lg text-white flex flex-col gap-2 max-w-[270px] h-[160px] rounded-lg">
    <h3 class="text-lg text-green-400">{{ title }}</h3>
    <p class="text-xs mt-4 leading-4 text-gray-400">{{ description }}</p>
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
