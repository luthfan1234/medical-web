<script setup lang="ts">
import Card from '@/components/ui/card/Card.vue';
import CardTitle from '@/components/ui/card/CardTitle.vue';
import CardDescription from '@/components/ui/card/CardDescription.vue';
import { ref } from 'vue';

const services = ref([
  {
    id: 1,
    title: 'Root Canal Treatment',
    description:
      'Root canal treatment (endodontics) is a dental procedure used to treat infection at the centre of a tooth.',
    icon: '/icon/services/icon-services-1.svg',
  },
  {
    id: 2,
    title: 'Cosmetic Dentist',
    description:
      'Cosmetic dentistry is the branch of dentistry that focuses on improving the appearance of your smile.',
    icon: '/icon/services/icon-services-2.svg',
  },
  {
    id: 3,
    title: 'Dental Implants',
    description:
      "A dental implant is an artificial tooth root that's placed into your jaw to hold a prosthetic tooth or bridge.",
    icon: '/icon/services/icon-services-3.svg',
  },
  {
    id: 4,
    title: 'Teeth Whitening',
    description:
      'Brighten your smile with safe and effective professional teeth whitening treatments.',
    icon: '/icon/services/icon-services-1.svg',
  },
  {
    id: 5,
    title: 'Orthodontic Braces',
    description:
      'Correct teeth alignment with our modern orthodontic solutions for all ages.',
    icon: '/icon/services/icon-services-2.svg',
  },
  {
    id: 6,
    title: 'Pediatric Dentistry',
    description:
      'Specialized dental care for children to ensure healthy smiles from an early age.',
    icon: '/icon/services/icon-services-3.svg',
  },
]);
</script>

<template>
  <div class="bg-soft-blue">
    <div class="flex items-center justify-center">
      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8"
      >
        <Card
          v-for="service in services"
          :key="service.id"
          class="w-full p-6 sm:p-8 border-none shadow-none flex flex-col items-center text-center bg-white rounded-xl"
        >
          <!-- icon -->
          <div class="flex justify-center items-center mb-4">
            <img :src="service.icon" :alt="service.title" class="w-16 h-16" />
          </div>

          <!-- title -->
          <CardTitle class="text-lg font-semibold text-deep-blue mb-2">
            {{ service.title }}
          </CardTitle>

          <!-- description -->
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed mb-4 text-center"
          >
            {{ service.description }}
          </CardDescription>

          <!-- button -->
          <button
            class="text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:circle-arrow-right" class="w-4 h-4" />
          </button>
        </Card>
      </div>
    </div>
  </div>
</template>
