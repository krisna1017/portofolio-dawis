<script setup lang="ts">
import Navbar from './components/Navbar.vue';
import HeroSection from './components/HeroSection.vue';
import AboutMeSection from './components/AboutMeSection.vue';
import ListProjectSection from './components/ListProjectSection.vue';
import ResumeSection from './components/ResumeSection.vue';
import FooterSection from './components/FooterSection.vue';
</script>

<template>
  <header>
    <Navbar />
  </header>

  <main>
    <HeroSection />
    <AboutMeSection />
    <ResumeSection />
    <ListProjectSection />
  </main>

  <footer>
    <FooterSection />
  </footer>
</template>
