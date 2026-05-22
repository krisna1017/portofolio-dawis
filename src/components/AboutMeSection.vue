<template>
  <section class="py-16 px-4 font-poppins bg-black from-gray-900 via-gray-800 to-gray-700 text-white" id="resume">
    <div class="container mx-auto flex flex-col md:flex-row items-center md:gap-12">
        <div class="relative flex flex-col max-w-md mb-12 md:mb-0 text-center justify-center">
            <span class="text-sm text-white font-light">Hello, I am</span>
            <h1 class="text-4xl text-white uppercase font-anton">Dawista</h1>
            <img src="../../public/image/section-2.png" class="ml-5" alt="about me image" />
            <div class="absolute inset-x-0 bottom-0 h-160 bg-linear-to-t from-black via-transparent to-transparent"></div>
        </div>
        <div class="flex flex-col max-w-2xl md:max-w-3xl px-8 md:px-0 gap-12">
            <div class="mb-4">
                <h2 class="text-4xl text-white font-anton mb-4">ABOUT ME</h2>
                <p class="text-lg leading-6 font-light">
                Hello I am Dawista, a Graphic Designer and UI/UX Designer focused on
                creating visually appealing, functional, and user-friendly designs. I have
                experience working on branding, social media content, and UI design for
                websites and mobile applications, as well as experience in Social Media
                Management (SMM) to combine design with more engaging content strategies.
                </p>
        </div>
            <div class="mb-4 w-full">
                <h2 class="text-4xl text-white font-anton">WHAT I DO?</h2>
                <div class="mt-6 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 place-items-center">
                    <Card
                        title="Graphic Design"
                        description="Creating visual designs for branding, social media content, posters, and other promotional materials with a clean and engaging style."
                    />
                    <Card
                        title="UI/UX Design"
                        description="Designing user-friendly and visually appealing interfaces for websites and mobile applications with a focus on user experience."
                    />
                    <Card
                        title="Social Media Specialist"
                        description="Managing social media content strategies, planning engaging posts, and helping brands build stronger online engagement."
                    />
                </div>
            </div>
        </div>
    </div>
    
  </section>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "AboutMeSection",
    components: {
    Card,
  },
};
</script>
