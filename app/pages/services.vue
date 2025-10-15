<script setup lang="ts">
import NavigationBarWhite from '~/components/NavigationBarWhite.vue';
import Footer from '~/components/Footer.vue';
import ServiceHeroSection from '~/components/services-screen/ServiceHeroSection.vue';
import ServicesPageSection from '~/components/services-screen/ServicesPageSection.vue';
import ServiceAppointmentSection from '~/components/services-screen/ServiceAppointmentSection.vue';
import ServicePlaylistSection from '~/components/services-screen/ServicePlaylistSection.vue';
</script>

<template>
  <div>
    <div class="px-20 py-10 font-sans bg-soft-blue">
      <NavigationBarWhite />
      <ServiceHeroSection />
      <ServicesPageSection />
    </div>

    <ServiceAppointmentSection />

    <div class="px-20">
      <ServicePlaylistSection />
      <Footer />
    </div>
  </div>
</template>
