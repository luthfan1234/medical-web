<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import NavigationBarWhite from '~/components/NavigationBarWhite.vue';
import AboutHeroSection from '~/components/about-screen/AboutHeroSection.vue';
import AboutMeetOurSpecialists from '~/components/about-screen/AboutMeetOurSpecialists.vue';
</script>

<template>
  <div class="px-20 py-10 font-sans bg-gradient-to-b from-soft-blue to-white">
    <NavigationBarWhite />
    <AboutHeroSection />
    <AboutMeetOurSpecialists />
    <Footer />
  </div>
</template>
