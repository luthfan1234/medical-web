<script setup lang="ts">
import { ref } from 'vue';
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from '@/components/ui/carousel';

const specialists = ref([
  {
    id: 1,
    name: 'Jim Carry',
    specialty: 'Orthodontist',
    image: '/images/docter1.png',
    linkedin: '#',
  },
  {
    id: 2,
    name: 'Wade Warren',
    specialty: 'Endodontist',
    image: '/images/docter2.png',
    linkedin: '#',
  },
  {
    id: 3,
    name: 'Jenny Wilson',
    specialty: 'Periodontist',
    image: '/images/docter3.png',
    linkedin: '#',
  },
  {
    id: 4,
    name: 'Jacob Jones',
    specialty: 'Pediatric Dentist',
    image: '/images/docter4.png',
    linkedin: '#',
  },
  {
    id: 5,
    name: 'Jacob Jones',
    specialty: 'Pediatric Dentist',
    image: '/images/docter4.png',
    linkedin: '#',
  },
  {
    id: 6,
    name: 'Jacob Jones',
    specialty: 'Pediatric Dentist',
    image: '/images/docter4.png',
    linkedin: '#',
  },
]);
</script>

<template>
  <div
    class="w-full flex flex-col text-center items-center justify-center bg-soft-blue py-16 sm:py-20 md:py-24 lg:py-32"
  >
    <!-- Title -->
    <div
      class="font-semibold text-3xl sm:text-4xl md:text-5xl text-deep-blue mb-5 px-4"
    >
      <h2>Meet Our Specialists</h2>
    </div>

    <p class="text-primary text-base lg:text-lg leading-relaxed px-4">
      We use only the best quality materials on the market in <br />order to
      provide the best products to our patients.
    </p>

    <!-- Carousel -->
    <div class="mt-12 w-full max-w-7xl px-4 sm:px-6 lg:px-8">
      <Carousel>
        <CarouselContent class="-ml-4 mb-5">
          <CarouselItem
            v-for="specialist in specialists"
            :key="specialist.id"
            class="pl-4 md:basis-1/2 lg:basis-1/3 xl:basis-1/4"
          >
            <div
              class="relative rounded-xl overflow-hidden bg-white w-full h-80 sm:h-86 flex flex-col"
            >
              <!-- Gambar Full -->
              <div class="relative w-full h-full">
                <img
                  :src="specialist.image"
                  :alt="specialist.name"
                  class="w-full h-full object-cover"
                />
                <!-- Tombol LinkedIn -->
                <a
                  :href="specialist.linkedin"
                  target="_blank"
                  class="absolute top-3 right-3"
                >
                  <img
                    src="/icon/icon-linkedin-specialist.svg"
                    alt="LinkedIn"
                    class="w-8 h-8 text-white"
                  />
                </a>
              </div>

              <!-- Info Dokter -->
              <div
                class="absolute left-3 right-3 bottom-3 sm:left-5 sm:right-5 sm:bottom-5 bg-gradient-to-r from-sky-blue to-light-gray text-left p-3 sm:p-4 rounded-lg"
              >
                <h3 class="text-white font-medium text-base sm:text-lg">
                  {{ specialist.name }}
                </h3>
                <p class="text-gray-200 text-sm sm:text-medium">
                  {{ specialist.specialty }}
                </p>
              </div>
            </div>
          </CarouselItem>
        </CarouselContent>

        <!-- Tombol navigasi -->
        <div
          class="flex gap-4 absolute -bottom-10 sm:-bottom-8 left-1/2 -translate-x-1/2 px-4 sm:px-14"
        >
          <CarouselPrevious
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-white hover:bg-gray-100 text-deep-blue border-none"
          />
          <CarouselNext
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-white hover:bg-gray-100 text-deep-blue border-none"
          />
        </div>
      </Carousel>
    </div>
  </div>
</template>
