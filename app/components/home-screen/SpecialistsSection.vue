<template>
  <div
    class="w-full h-[47rem] flex flex-col text-center items-center justify-center bg-soft-blue"
  >
    <!-- Title -->
    <div class="font-semibold text-5xl text-deep-blue mb-5">
      <h2>Meet Our <span class="font-bold">Specialists</span></h2>
    </div>

    <p class="text-gray-600">
      We use only the best quality materials on the market in order <br />
      to provide the best products to our patients.
    </p>

    <!-- Carousel -->
    <div class="w-full max-w-6xl mt-12">
      <Carousel class="w-full">
        <CarouselContent>
          <CarouselItem
            v-for="specialist in specialists"
            :key="specialist.id"
            class="md:basis-1/2 lg:basis-1/4"
          >
            <div class="relative rounded-xl overflow-hidden shadow-lg">
              <!-- Doctor photo -->
              <img
                :src="specialist.image"
                :alt="specialist.name"
                class="w-full h-[22rem] object-cover"
              />

              <!-- LinkedIn button -->
              <a
                :href="specialist.linkedin"
                target="_blank"
                class="absolute top-3 right-3 bg-white p-1 rounded-full shadow hover:bg-gray-100"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                  class="w-5 h-5 text-deep-blue"
                >
                  <path
                    d="M4.98 3.5C4.98 4.88 3.88 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1 4.98 2.12 4.98 3.5zM.16 8h4.67v16H.16zM8.34 8h4.47v2.17h.06c.62-1.17 2.14-2.4 4.41-2.4 4.72 0 5.59 3.1 5.59 7.12V24h-4.67v-7.74c0-1.85-.03-4.23-2.58-4.23-2.59 0-2.99 2.02-2.99 4.1V24H8.34V8z"
                  />
                </svg>
              </a>

              <!-- Doctor info -->
              <div
                class="absolute bottom-0 w-full bg-gradient-to-t from-gray-900/70 to-transparent text-left p-4"
              >
                <h3 class="text-white font-semibold text-lg">
                  {{ specialist.name }}
                </h3>
                <p class="text-gray-200 text-sm">{{ specialist.specialty }}</p>
              </div>
            </div>
          </CarouselItem>
        </CarouselContent>

        <!-- Navigation buttons placed inside carousel so controls have access to context -->
        <div class="flex justify-center gap-4 mt-6 w-full">
          <CarouselPrevious
            class="inline-flex items-center justify-center w-11 h-11 rounded-full bg-white shadow hover:bg-gray-100 text-deep-blue"
            aria-label="Previous"
          >
            <!-- left arrow -->
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-5 h-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 19l-7-7 7-7"
              />
            </svg>
          </CarouselPrevious>

          <CarouselNext
            class="inline-flex items-center justify-center w-11 h-11 rounded-full bg-white shadow hover:bg-gray-100 text-deep-blue"
            aria-label="Next"
          >
            <!-- right arrow -->
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-5 h-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 5l7 7-7 7"
              />
            </svg>
          </CarouselNext>
        </div>
      </Carousel>
    </div>
  </div>
</template>

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
    image: '/images/doc1.png',
    linkedin: '#',
  },
  {
    id: 2,
    name: 'Wade Warren',
    specialty: 'Endodontist',
    image: '/images/doc2.png',
    linkedin: '#',
  },
  {
    id: 3,
    name: 'Jenny Wilson',
    specialty: 'Periodontist',
    image: '/images/doc3.png',
    linkedin: '#',
  },
  {
    id: 4,
    name: 'Jacob Jones',
    specialty: 'Pediatric Dentist',
    image: '/images/doc4.png',
    linkedin: '#',
  },
]);
</script>
