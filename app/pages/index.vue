<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import HeroSection from '~/components/home-screen/HeroSection.vue';
import WelcomeSection from '~/components/home-screen/WelcomeSection.vue';
import WhyChooseUsSection from '~/components/home-screen/WhyChooseUsSection.vue';

import NavigationBar from '~/components/NavigationBar.vue';
</script>

<template>
  <div class="px-20 py-10 font-sans">
    <NavigationBar />
    <HeroSection />
    <WelcomeSection />
    <WhyChooseUsSection />
    <Footer />
  </div>
</template>
