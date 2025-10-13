<script setup lang="ts">
import { ref } from 'vue';
import { Linkedin } from 'lucide-vue-next';
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
    class="w-full h-[47rem] flex flex-col text-center items-center justify-center bg-soft-blue"
  >
    <!-- Title -->
    <div class="font-semibold text-5xl text-deep-blue mb-5">
      <h2>Meet Our <span class="font-bold">Specialists</span></h2>
    </div>

    <p class="text-primary">
      We use only the best quality materials on the market in order <br />
      to provide the best products to our patients.
    </p>

    <!-- Carousel -->
    <div class="mt-12 w-full max-w-7xl px-4">
      <Carousel>
        <CarouselContent class="-ml-4 mb-5">
          <CarouselItem
            v-for="specialist in specialists"
            :key="specialist.id"
            class="pl-4 md:basis-1/2 lg:basis-1/3 xl:basis-1/4"
          >
            <div
              class="relative rounded-xl overflow-hidden bg-white w-full h-[25rem] flex flex-col"
            >
              <!-- Gambar Full -->
              <div class="relative w-full h-full">
                <img
                  :src="specialist.image"
                  :alt="specialist.name"
                  class="w-full h-full object-cover"
                />
                <!-- Tombol LinkedIn -->
                <a>
                  :href="specialist.linkedin" target="_blank" class="absolute
                  top-3 right-3 bg-primary p-1.5 flex items-center
                  justify-center rounded-md hover:bg-primary/90 transition" >
                  <Linkedin class="w-5 h-5 text-white" />
                </a>
              </div>

              <!-- Info Dokter -->
              <div
                class="absolute left-5 right-5 bottom-5 bg-gradient-to-r from-sky-blue to-light-gray text-left p-4 rounded-lg"
              >
                <h3 class="text-white font-regular text-lg">
                  {{ specialist.name }}
                </h3>
                <p class="text-gray-200 text-regular">
                  {{ specialist.specialty }}
                </p>
              </div>
            </div>
          </CarouselItem>
        </CarouselContent>

        <!-- Tombol navigasi -->
        <div
          class="flex gap-4 absolute -bottom-8 left-1/2 -translate-x-1/2 px-14"
        >
          <CarouselPrevious
            class="inline-flex items-center justify-center w-24 h-11 rounded-none bg-white hover:bg-gray-100 text-deep-blue border-none"
          />
          <CarouselNext
            class="inline-flex items-center justify-center w-24 h-11 rounded-none bg-white hover:bg-gray-100 text-deep-blue border-none"
          />
        </div>
      </Carousel>
    </div>
  </div>
</template>
