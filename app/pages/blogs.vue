<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import NavigationBarWhite from '~/components/NavigationBarWhite.vue';
import BlogsArticlesSection from '~/components/blogs-screen/BlogsArticlesSection.vue';
import BlogsCarouselSection from '~/components/blogs-screen/BlogsCarouselSection.vue';
import BlogsHeroSection from '~/components/blogs-screen/BlogsHeroSection.vue';
import BlogsPlaylistSection from '~/components/blogs-screen/BlogsPlaylistSection.vue';
import BlogsFAQSection from '~/components/blogs-screen/BlogsFAQSection.vue';
import BlogsPromoSection from '~/components/blogs-screen/BlogsPromoSection.vue';
</script>

<template>
  <div class="px-20 py-10 font-sans bg-gradient-to-b from-soft-blue to-white">
    <NavigationBarWhite />
    <BlogsHeroSection />
    <BlogsCarouselSection />
    <BlogsArticlesSection />
    <BlogsPlaylistSection />
    <BlogsFAQSection />
    <BlogsPromoSection />
    <Footer />
  </div>
</template>
