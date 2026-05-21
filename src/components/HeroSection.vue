<template>
  <section class="h-screen flex flex-col items-center justify-center text-center from-gray-900 via-gray-800 to-gray-700 text-white relative">
    <div class="flex flex-col items-center gap-4">
      <ProfileImage class="w-36 h-36 rounded-full overflow-hidden mb-4" />
      <h1 class="text-7xl font-extrabold uppercase">portofolio</h1>
      <p class="text-lg font-bold mt-4">DESIGN GRAPHIC & UI/UX DESIGN</p>
      <button class="mt-6 bg-green-500 text-white py-3 px-6 rounded-full text-lg font-semibold hover:bg-green-400 transition">
        MORE ABOUT ME
      </button>
    </div>
  </section>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";

export default {
  name: "HeroSection",
  components: {
    ProfileImage,
  },
};
</script>