<script setup lang="ts">
import NavigationBarWhite from '~/components/NavigationBarWhite.vue';
import Footer from '~/components/Footer.vue';
import HeroServiceSection from '~/components/services-screen/HeroServiceSection.vue';
import ServicesPageSection from '~/components/services-screen/ServicesPageSection.vue';
import AppointmentSection from '~/components/services-screen/AppointmentSection.vue';
</script>

<template>
  <div>
    <div class="px-20 py-10 font-sans bg-soft-blue">
      <NavigationBarWhite />
      <HeroServiceSection />
      <ServicesPageSection />
    </div>

    <AppointmentSection />
    
    <div class="px-20">
      <Footer />
    </div>
  </div>
</template>
