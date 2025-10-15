<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import BlogsCarouselSection from '~/components/blogs-screen/BlogsCarouselSection.vue';
import BlogsHeroSection from '~/components/blogs-screen/BlogsHeroSection.vue';
</script>

<template>
  <div class="px-20 py-10 font-sans bg-gradient-to-b from-soft-blue to-white">
    <NavigationBarWhite />
    <BlogsHeroSection />
    <BlogsCarouselSection />
    <Footer />
  </div>
</template>
