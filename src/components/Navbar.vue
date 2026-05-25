<template>
  <nav :class="['w-full h-20 hidden md:flex justify-center items-center fixed top-0 z-50 transition-all duration-300', isScrolled ? 'bg-black/20 backdrop-blur-sm' : 'bg-transparent']">
    <ul class="flex gap-2 md:gap-8 list-none">
      <li>
        <a
          href="#profile"
          @click="setActive('#profile')"
          :class="[
            'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl',
            activeMenu === '#profile' ? 'bg-green-600' : 'hover:bg-green-600'
          ]"
        >
          PROFILE
        </a>
      </li>

      <li>
        <a
          href="#resume"
          @click="setActive('#resume')"
          :class="[
            'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl',
            activeMenu === '#resume' ? 'bg-green-600' : 'hover:bg-green-600'
          ]"
        >
          RESUME
        </a>
      </li>

      <li>
        <a
          href="#project"
          @click="setActive('#project')"
          :class="[
            'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl',
            activeMenu === '#project' ? 'bg-green-600' : 'hover:bg-green-600'
          ]"
        >
          PROJECT
        </a>
      </li>

      <li>
        <a
          href="#contact"
          @click="setActive('#contact')"
          :class="[
            'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl',
            activeMenu === '#contact' ? 'bg-green-600' : 'hover:bg-green-600'
          ]"
        >
          CONTACT
        </a>
      </li>
    </ul>
  </nav>

  <!-- drawer init and toggle -->
  <div :class="['w-full h-20 hidden max-sm:flex justify-end items-center fixed top-0 z-50 transition-all duration-300', isScrolled ? 'bg-black/20 backdrop-blur-sm' : 'bg-transparent']">
    <button @click="toggleDrawer" class=" items-center justify-center text-white box-border border border-transparent hover:bg-amber-strong focus:ring-4 focus:ring-amber-medium shadow-xs font-medium leading-5 rounded-base text-sm px-4 py-2.5 focus:outline-none" type="button">
      <svg v-if="!isDrawerOpen" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-8 stroke-olive-50 stroke-1">
        <path fill-rule="evenodd" d="M3 6.75A.75.75 0 0 1 3.75 6h16.5a.75.75 0 0 1 0 1.5H3.75A.75.75 0 0 1 3 6.75ZM3 12a.75.75 0 0 1 .75-.75h16.5a.75.75 0 0 1 0 1.5H3.75A.75.75 0 0 1 3 12Zm0 5.25a.75.75 0 0 1 .75-.75h16.5a.75.75 0 0 1 0 1.5H3.75a.75.75 0 0 1-.75-.75Z" clip-rule="evenodd" />
      </svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-8 stroke-olive-50 stroke-1">
          <path fill-rule="evenodd" d="M5.47 5.47a.75.75 0 0 1 1.06 0L12 10.94l5.47-5.47a.75.75 0 1 1 1.06 1.06L13.06 12l5.47 5.47a.75.75 0 1 1-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 0 1-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 0 1 0-1.06Z" clip-rule="evenodd" />
        </svg>
    </button>
  </div>

  <!-- drawer component -->
  <div v-if="isDrawerOpen" class="fixed top-0 right-0 hidden max-sm:inline-flex justify-center items-center z-40 h-screen p-4 overflow-y-hidden transition-transform bg-black w-full text-center" tabindex="-1" aria-labelledby="drawer-right-label">
    <ul class="flex flex-col gap-8 list-none">
      <li>
        <a href="#profile">
          <button
            @click="setActive('#profile')"
            :class="[
              'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl text-lg',
              activeMenu === '#profile' ? 'bg-green-600' : 'hover:bg-green-600'
            ]"
          >
            PROFILE
          </button>
        </a>
      </li>
      <li>
        <a href="#resume">
                    <button
            @click="setActive('#resume')"
            :class="[
              'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl text-lg',
              activeMenu === '#resume' ? 'bg-green-600' : 'hover:bg-green-600'
            ]"
          >
            RESUME
          </button>
        </a>
      </li>
      <li>
        <a href="#project">
          <button
            @click="setActive('#project')"
            :class="[
              'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl text-lg',
              activeMenu === '#project' ? 'bg-green-600' : 'hover:bg-green-600'
            ]"
          >
            PROJECT
          </button>
        </a>
      </li>
      <li>
        <a href="#contact">
          <button
            @click="setActive('#contact')"
            :class="[
              'text-white transition-all duration-300 font-light px-3 py-1 rounded-xl text-lg',
              activeMenu === '#contact' ? 'bg-green-600' : 'hover:bg-green-600'
            ]"
          >
            CONTACT
          </button>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      isScrolled: false,
      isDrawerOpen: false,
      activeMenu: "#",
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
    toggleDrawer() {
      this.isDrawerOpen = !this.isDrawerOpen;
    },
    closeDrawer() {
      this.isDrawerOpen = false;
    },
    setActive(menu) {
      this.activeMenu = menu;
      this.closeDrawer();
    },
  },
};
</script>