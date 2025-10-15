<template>
  <div
    class="w-full flex flex-col text-center items-center justify-center py-5 sm:py-5 md:py-5 lg:py-5 bg-white"
  >
    <h2
      class="font-semibold text-3xl sm:text-4xl md:text-5xl text-deep-blue mb-5 px-4 mt-16"
    >
      Frequently Ask Question
    </h2>
    <p class="text-gray-600 text-base lg:text-lg leading-relaxed px-4 mb-12">
      We use only the best quality materials on the market in order to
      <br class="hidden sm:block" />
      provide the best products to our patients.
    </p>

    <div class="w-full max-w-2xl space-y-4">
      <div
        v-for="(faq, index) in faqs"
        :key="index"
        class="w-full rounded-xl px-8 py-4 cursor-pointer transition-all duration-300"
        :class="faq.isOpen ? 'bg-bright-blue text-white' : 'text-primary'"
        @click="toggleFAQ(index)"
      >
        <div class="flex justify-between items-center">
          <h3 class="font-medium">• {{ faq.question }}</h3>
          <div>
            <Icon
              :name="faq.isOpen ? 'lucide:circle-minus' : 'lucide:circle-plus'"
              class="w-6 h-6"
            />
          </div>
        </div>

        <hr
          class="my-5 border-t-2 transition-colors duration-300"
          :class="faq.isOpen ? 'border-white' : 'border-ring opacity-30'"
        />

        <Transition name="fade-slide">
          <p v-if="faq.isOpen" class="text-left">
            {{ faq.answer }}
          </p>
        </Transition>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface FAQ {
  question: string;
  answer: string;
  isOpen: boolean;
}

const faqs = ref<FAQ[]>([
  {
    question: 'Can I see who reads my email campaigns?',
    answer:
      'Yes, our email marketing platform provides detailed analytics that allow you to track who opens your emails, clicks on links, and engages with your content. You can view reports that show the number of opens, click-through rates, and even the geographic location of your subscribers. This information helps you understand your audience better and tailor future campaigns to their interests.',
    isOpen: true,
  },
  {
    question: 'Do you offer non-profit discounts?',
    answer:
      'Yes, we offer special pricing for qualified non-profit organizations. Please contact our sales team with your non-profit documentation to learn more about available discounts and how to apply them to your account.',
    isOpen: false,
  },
  {
    question: 'How secure is my data?',
    answer:
      'We take data security very seriously. All data is encrypted both in transit and at rest, and we comply with industry standards including GDPR and CCPA. Our platform undergoes regular security audits and we maintain SOC 2 Type II certification.',
    isOpen: false,
  },
  {
    question: 'Can I integrate with other tools?',
    answer:
      'Absolutely! We offer integrations with popular CRM systems, e-commerce platforms, and marketing tools. Our API also allows for custom integrations to fit your specific workflow needs.',
    isOpen: false,
  },
]);

const toggleFAQ = (index: number) => {
  if (faqs.value[index]) {
    faqs.value[index].isOpen = !faqs.value[index].isOpen;
  }
};
</script>

<style scoped>
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.3s ease;
}

.fade-slide-enter-from {
  opacity: 0;
  transform: translateY(-10px);
}

.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
