<template>
  <section class="py-16 px-4">
    <div class="container mx-auto flex flex-row items-center md:gap-12">
        <div class="flex flex-col max-w-md mb-12 md:mb-0 text-center justify-center">
            <span>Hello, I am</span>
            <h1 class="text-4xl font-bold text-white uppercase">Dawista</h1>
            <img src="../../public/image/section-2.png" alt="">
        </div>
        <div class="flex flex-col max-w-3xl gap-6">
            <h2 class="text-4xl font-extrabold text-white">ABOUT ME</h2>
            <p class="text-lg leading-6 font-light">
            Hello I am Dawista, a Graphic Designer and UI/UX Designer focused on
            creating visually appealing, functional, and user-friendly designs. I have
            experience working on branding, social media content, and UI design for
            websites and mobile applications, as well as experience in Social Media
            Management (SMM) to combine design with more engaging content strategies.
            </p>
            <h2 class="text-4xl font-bold text-white">WHAT I DO?</h2>
            <div class="mt-6 flex flex-col md:flex-row gap-4">
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
