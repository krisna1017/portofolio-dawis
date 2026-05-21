<template>
  <section class="h-screen flex flex-col items-center justify-center text-center bg-black from-gray-900 via-gray-800 to-gray-700 text-white relative font-poppins">
    <div class="flex flex-col items-center gap-4">
      <ProfileImage class="w-36 h-36 rounded-full overflow-hidden mb-4" />
      <h1 class="text-8xl uppercase font-anton">portofolio</h1>
      <p class="text-sm font-thin">DESIGN GRAPHIC & UI/UX DESIGN</p>
      <button class="mt-6 bg-green-600 text-white py-3 px-6 rounded-full text-lg font-bold hover:bg-green-500 transition">
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