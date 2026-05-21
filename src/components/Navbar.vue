<template>
  <nav :class="['w-full h-20 flex justify-center items-center fixed top-0 z-50 transition-all duration-300', isScrolled ? 'bg-black/70 backdrop-blur-(100px)' : 'bg-transparent']">
    <ul class="flex gap-8 list-none">
      <li><a href="#profile" class="text-white hover:bg-green-400 transition-all duration-300 font-light px-3 py-1 rounded-xl">PROFILE</a></li>
      <li><a href="#resume" class="text-white hover:bg-green-400 transition-all duration-300 font-light px-3 py-1 rounded-xl">RESUME</a></li>
      <li><a href="#project" class="text-white hover:bg-green-400 transition-all duration-300 font-light px-3 py-1 rounded-xl">PROJECT</a></li>
      <li><a href="#contact" class="text-white hover:bg-green-400 transition-all duration-300 font-light px-3 py-1 rounded-xl">CONTACT</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isScrolled: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 0;
    },
  },
};
</script>