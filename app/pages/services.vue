<script setup lang="ts">
import NavigationBarWhite from '~/components/NavigationBarWhite.vue';
import Footer from '~/components/Footer.vue';
import ServiceHeroSection from '~/components/services-screen/ServiceHeroSection.vue';
import ServicesPageSection from '~/components/services-screen/ServicesPageSection.vue';
import ServiceAppointmentSection from '~/components/services-screen/ServiceAppointmentSection.vue';
import ServicePlaylistSection from '~/components/services-screen/ServicePlaylistSection.vue';
import ServiceSpecialistsSection from '~/components/services-screen/ServiceSpecialistsSection.vue';
import ServiceFAQSection from '~/components/services-screen/ServiceFAQSection.vue';
import ServicePromoSection from '~/components/services-screen/ServicePromoSection.vue';
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
    </div>

    <ServiceSpecialistsSection />

    <div class="px-20">
      <ServiceFAQSection />
      <ServicePromoSection />
      <Footer />
    </div>
  </div>
</template>
