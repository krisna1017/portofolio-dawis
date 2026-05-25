<template>
    <section class="relative z-10 py-16 px-4 font-poppins bg-black from-gray-900 via-gray-800 to-gray-700 text-white h-full" id="project">

      <!-- Background Vector Images left top-->
      <div class="absolute -top-100 left-0 rotate-180">
        <img src="/image/vector-4.png" class="w-96 h-200 max-sm:w-48 max-sm:h-180 object-fill blur-2xl" alt="hero section image" />
      </div>

      <!-- Background Vector Images right bottom -->
      <div class="absolute -bottom-100 right-0 h-full w-full rotate-180">
        <img src="../../public/image/vector-3.png" class="w-96 h-200 max-sm:w-48 max-sm:h-150 object-fill blur-2xl" alt="hero section image" />
      </div>

      <div class="container mx-auto relative">
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
                  activeTab === tab ? 'underline underline-offset-8 decoration-green-600 text-gray-300' : 'text-gray-500 hover:text-gray-300 hover:bg-white/10'
                ]"
              >
                {{ tab }}
              </button>
            </div>
          </div>

          <transition name="fade" mode="out-in">
            <div :key="activeTab" class="grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
              <article
                v-for="(project, index) in filteredProjects"
                :key="project.title"
                :class="[
                  'group overflow-hidden rounded-3xl border border-white/10 bg-white/5 p-4 shadow-[0_20px_60px_rgba(255,255,255,0.04)] transition duration-500 hover:-translate-y-1 hover:border-white/20 backdrop-blur-4xl',
                  activeTab === 'SOCIAL MEDIA' && index === 0
                    ? 'sm:col-span-2 lg:col-span-2'
                    : index === filteredProjects.length - 1 && filteredProjects.length % 4 === 1
                      ? 'sm:col-span-2 lg:col-span-2'
                      : '',
                  activeTab === 'SOCIAL MEDIA' && index === 1
                    ? 'sm:col-span-2 lg:col-span-2'
                    : index === filteredProjects.length - 1 && filteredProjects.length % 4 === 1
                      ? 'sm:col-span-2 lg:col-span-2'
                      : ''
                ]"
              >
                <div
                  class="h-64 w-full bg-contain bg-no-repeat bg-center transition duration-700 group-hover:scale-105"
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
    image: "url('/image/design-graphic/design graphic/1.png')"
  },
  {
    title: 'Giveaway Campaign',
    category: 'DESIGN GRAPHIC',
    description: 'Eye-catching social giveaway design with bright branding.',
    tags: ['Social', 'Promo'],
    image: "url('/image/design-graphic/design graphic/2.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/3.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/4.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/5.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/6.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/7.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/8.png')"
  },
  {
    title: 'Perlokok Peduli',
    category: 'DESIGN GRAPHIC',
    description: 'Brand campaign layout with custom typography and texture.',
    tags: ['Branding', 'Layout'],
    image: "url('/image/design-graphic/design graphic/9.png')"
  },
  {
    title: 'New Year Launch',
    category: 'SOCIAL MEDIA',
    description: 'Animated social tile series optimized for engagement.',
    tags: ['Instagram', 'Campaign'],
    image: "url('/image/sosmed/sosmed/1.png')",
  },
  {
    title: 'Balonku Babyshop',
    category: 'SOCIAL MEDIA',
    description: 'Creative promotional carousel for product awareness.',
    tags: ['Carousel', 'Content'],
    image: "url('/image/sosmed/sosmed/2.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/1.png')"
  },
  {
    title: 'Dashboard Prototype',
    category: 'UI/UX DESIGN',
    description: 'Data dashboard layout with clean visual hierarchy.',
    tags: ['Dashboard', 'UX'],
    image: "url('/image/ui-ux/ui-ux/2.jpg')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/3.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/4.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/5.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/6.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/7.png')"
  },
  {
    title: 'Travel App UI',
    category: 'UI/UX DESIGN',
    description: 'Modern mobile interface designed for easy booking flow.',
    tags: ['Figma', 'App'],
    image: "url('/image/ui-ux/ui-ux/8.png')"
  },
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
