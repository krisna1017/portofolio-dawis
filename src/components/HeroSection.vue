<template>
  <section class="py-16 px-4 h-screen flex flex-col items-center justify-center text-center bg-black from-gray-900 via-gray-800 to-gray-700 text-white relative font-poppins" id="profile">
    <div class="flex flex-col items-center gap-4 z-10">
      <ProfileImage class="w-36 h-36 rounded-full overflow-hidden mb-4 hidden md:block" />
      <h1 class="text-7xl md:text-8xl lg:text-8xl uppercase font-anton">portofolio</h1>
      <p class="text-sm font-thin">DESIGN GRAPHIC & UI/UX DESIGN</p>
      <button @click="scrollToAbout" class="mt-6 bg-green-600 text-white py-3 px-6 rounded-full text-lg font-bold hover:bg-green-500 transition">
        MORE ABOUT ME
      </button>
    </div>
   <div class="absolute top-0 left-0 h-full w-full">
    <img src="../../public/image/vector-1.png" class="w-full h-200 max-sm:h-350 object-cover max-sm:object-fill blur-2xl" alt="hero section image" />
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
  methods: {
    scrollToAbout() {
      const el = document.getElementById('about');
      if (el) el.scrollIntoView({ behavior: 'smooth' });
    }
  }
};
</script>