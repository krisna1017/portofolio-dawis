<template>
  <section class="py-16 px-4 h-screen flex flex-col items-center justify-center text-center bg-black from-gray-900 via-gray-800 to-gray-700 text-white relative font-poppins" id="hero">
    <div class="flex flex-col items-center gap-4 z-10">
      <!-- <ProfileImage class="w-36 h-36 rounded-full overflow-hidden mb-4 hidden lg:block" /> -->
      <h1 class="text-7xl md:text-8xl lg:text-8xl uppercase font-anton">portofolio</h1>
      <TypingText />
      <button @click="scrollToAbout" class="mt-6 bg-green-600 text-white py-3 px-6 rounded-full text-lg font-bold hover:bg-green-500 transition">
        MORE ABOUT ME
      </button>
    </div>
   <div class="absolute -bottom-50 left-0 h-full w-full">
    <img src="../../public/image/vector-1.png" class="w-full h-full max-md:h-350 object-cover max-md:object-fill blur-2xl" alt="hero section image" />
   </div>
  </section>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import TypingText from "./TypingText.vue";

export default {
  name: "HeroSection",
  components: {
    ProfileImage,
    TypingText,
  },
  methods: {
    scrollToAbout() {
      const el = document.getElementById('profile');
      if (el) el.scrollIntoView({ behavior: 'smooth' });
    }
  }
};
</script>