<script setup lang="ts">
import Footer from '~/components/Footer.vue';
import NavigationBar from '~/components/NavigationBar.vue';
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
