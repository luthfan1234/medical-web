<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import HeroSection from '~/components/home-screen/HeroSection.vue';
import WelcomeSection from '~/components/home-screen/WelcomeSection.vue';
import WhyChooseUsSection from '~/components/home-screen/WhyChooseUsSection.vue';
import CTASection from '~/components/home-screen/CTASection.vue';
import NavigationBar from '~/components/NavigationBar.vue';
import SpecialistsSection from '~/components/home-screen/SpecialistsSection.vue';
import PlaylistSection from '~/components/home-screen/PlaylistSection.vue';
import TestimonialsSection from '~/components/home-screen/TestimonialsSection.vue';
import ArticleSection from '~/components/home-screen/ArticlesSection.vue';
import FAQSection from '~/components/home-screen/FAQSection.vue';
import PromoSection from '~/components/home-screen/PromoSection.vue';
</script>

<template>
  <div>
    <div class="px-20 py-10 font-sans">
      <NavigationBar />
      <HeroSection />
      <WelcomeSection />
      <WhyChooseUsSection />
      <CTASection />
      <PlaylistSection />
    </div>

    <!-- Section tanpa padding -->
    <SpecialistsSection />

    <div class="px-20">
      <!-- <TestimonialsSection /> -->
      <TestimonialsSection />
      <ArticleSection />
      <FAQSection />
      <PromoSection />
      <Footer />
    </div>
  </div>
</template>
