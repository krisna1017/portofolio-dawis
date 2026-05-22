<template>
  <section class="py-16 px-4 font-poppins bg-black from-gray-900 via-gray-800 to-gray-700 text-white" id="project">
    <div class="container mx-auto">
      <div class="flex flex-col gap-10">
        <div class="flex flex-col items-center gap-4">
          <div class="inline-flex flex-wrap items-center justify-center gap-3 md:gap-6 lg:gap-12 rounded-full p-2 shadow-[0_0_40px_rgba(255,255,255,0.03)]">
            <button
              v-for="tab in tabs"
              :key="tab"
              type="button"
              @click="activeTab = tab"
              :class="[
                'rounded-full px-5 py-3 text-2xl font-regular tracking-wider font-anton transition duration-300',
                activeTab === tab ? 'underline underline-offset-8 text-gray-300' : 'text-gray-500 hover:text-gray-300 hover:bg-white/10'
              ]"
            >
              {{ tab }}
            </button>
          </div>
        </div>

        <transition name="fade" mode="out-in">
          <div :key="activeTab" class="grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
            <article
              v-for="project in filteredProjects"
              :key="project.title"
              class="group overflow-hidden rounded-3xl border border-white/10 bg-white/5 p-4 shadow-[0_20px_60px_rgba(255,255,255,0.04)] transition duration-500 hover:-translate-y-1 hover:border-white/20"
            >
              <div
                class="aspect-[4/5] w-full overflow-hidden rounded-3xl bg-cover bg-center transition duration-700 group-hover:scale-105"
                :style="{ backgroundImage: project.image }"
              ></div>
              <div class="mt-5 flex flex-col gap-3">
                <span class="inline-flex rounded-full bg-white/10 px-3 py-1 text-xs uppercase tracking-[0.25em] text-slate-300">
                  {{ project.category }}
                </span>
                <h3 class="text-lg font-semibold text-white">{{ project.title }}</h3>
                <p class="text-sm leading-6 text-slate-300">{{ project.description }}</p>
                <div class="flex flex-wrap gap-2 pt-2">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="rounded-full bg-white/10 px-3 py-1 text-[11px] uppercase tracking-[0.25em] text-slate-300"
                  >
                    {{ tag }}
                  </span>
                </div>
              </div>
            </article>
          </div>
        </transition>
      </div>
    </div>
  </section>
</template>

<script setup>
import { computed, ref } from 'vue';

const tabs = [
  'DESIGN GRAPHIC',
  'UI/UX DESIGN',
  'SOCIAL MEDIA'
];

const activeTab = ref('DESIGN GRAPHIC');

const projects = [
  {
    title: 'Progr(a)mming 7.1',
    category: 'DESIGN GRAPHIC',
    description: 'Digital poster and visual identity for event promotion.',
    tags: ['Poster', 'Illustration'],
    image: 'linear-gradient(135deg, rgba(79,70,229,0.95), rgba(0,0,0,0.4))'
  },
  {
    title: 'Giveaway Campaign',
    category: 'DESIGN GRAPHIC',
    description: 'Eye-catching social giveaway design with bright branding.',
    tags: ['Social', 'Promo'],
    image: 'linear-gradient(135deg, rgba(16,185,129,0.95), rgba(0,0,0,0.35))'
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: 'linear-gradient(135deg, rgba(16,185,129,0.95), rgba(17,24,39,0.45))'
  },
  {
    title: 'New Year Launch',
    category: 'SOCIAL MEDIA',
    description: 'Animated social tile series optimized for engagement.',
    tags: ['Instagram', 'Campaign'],
    image: 'linear-gradient(135deg, rgba(59,130,246,0.95), rgba(15,23,42,0.45))'
  },
  {
    title: 'Balonku Babyshop',
    category: 'SOCIAL MEDIA',
    description: 'Creative promotional carousel for product awareness.',
    tags: ['Carousel', 'Content'],
    image: 'linear-gradient(135deg, rgba(249,115,22,0.95), rgba(15,23,42,0.45))'
  },
  {
    title: 'BOM Agency Drive',
    category: 'SOCIAL MEDIA',
    description: 'Campaign design for organic growth and reach.',
    tags: ['Brand', 'Social'],
    image: 'linear-gradient(135deg, rgba(236,72,153,0.95), rgba(15,23,42,0.45))'
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: 'linear-gradient(135deg, rgba(14,165,233,0.95), rgba(15,23,42,0.45))'
  },
  {
    title: 'Dashboard Prototype',
    category: 'UI/UX DESIGN',
    description: 'Data dashboard layout with clean visual hierarchy.',
    tags: ['Dashboard', 'UX'],
    image: 'linear-gradient(135deg, rgba(168,85,247,0.95), rgba(15,23,42,0.45))'
  }
];

const filteredProjects = computed(() => projects.filter((project) => project.category === activeTab.value));
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.35s ease, transform 0.35s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(18px);
}
</style>
