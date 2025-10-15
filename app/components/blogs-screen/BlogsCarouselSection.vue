<script setup lang="ts">
import { ref } from 'vue';
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from '@/components/ui/carousel';

const blogs = ref([
  {
    id: 1,
    title: 'Why You Should Choose a Pediatric Dentist',
    description:
      'Pediatric dentists are dental specialists who focus on the oral health of children from infancy through adolescence.',
    image: '/images/blogs/blog1.png',
    link: '#',
  },
  {
    id: 2,
    title: 'The Importance of Oral Hygiene for Children',
    description:
      'Good oral hygiene is essential for maintaining healthy teeth and gums. Children should be taught proper oral hygiene habits from an early age.',
    image: '/images/blogs/blog2.png',
    link: '#',
  },
  {
    id: 3,
    title: 'The Benefits of Dental Sealants for Children',
    description:
      'Dental sealants are a thin layer of material applied to the teeth to prevent tooth decay. They are an effective way to prevent cavities from forming on the teeth.',
    image: '/images/blogs/blog3.png',
    link: '#',
  },
  {
    id: 4,
    title: 'Why You Should Choose a Pediatric Dentist',
    description:
      'Pediatric dentists are dental specialists who focus on the oral health of children from infancy through adolescence.',
    image: '/images/blogs/blog4.png',
    link: '#',
  },
  {
    id: 5,
    title: 'The Importance of Oral Hygiene for Children',
    description:
      'Good oral hygiene is essential for maintaining healthy teeth and gums. Children should be taught proper oral hygiene habits from an early age.',
    image: '/images/blogs/blog5.png',
    link: '#',
  },
  {
    id: 6,
    title: 'The Benefits of Dental Sealants for Children',
    description:
      'Dental sealants are a thin layer of material applied to the teeth to prevent tooth decay. They are an effective way to prevent cavities from forming on the teeth.',
    image: '/images/blogs/blog6.png',
    link: '#',
  },
]);
</script>

<template>
  <div
    class="w-full flex flex-col text-center items-center justify-center bg-soft-blue py-16 sm:py-20 md:py-24 lg:py-32"
  >
    <!-- Carousel -->
    <div class="w-full max-w-7xl px-4 sm:px-6 lg:px-8">
      <Carousel>
        <CarouselContent class="-ml-3 mb-18">
          <CarouselItem
            v-for="blog in blogs"
            :key="blog.id"
            class="pl-3 md:basis-1/2 lg:basis-1/3 xl:basis-1/4"
          >
            <div
              class="relative rounded-xl overflow-hidden bg-white w-full h-82 flex flex-col"
            >
              <div class="relative w-full h-full">
                <img
                  :src="blog.image"
                  :alt="blog.title"
                  class="w-full h-full object-cover"
                />
              </div>

              <div
                class="absolute left-3 right-3 bottom-3 sm:left-5 sm:right-5 sm:bottom-5 bg-gradient-to-r from-sky-blue to-light-gray text-left p-3 sm:p-4 rounded-lg"
              >
                <h3 class="text-white font-semibold text-base sm:text-lg">
                  {{ blog.title }}
                </h3>
                <p class="text-gray-200 text-sm">
                  {{ blog.description }}
                </p>
              </div>
            </div>
          </CarouselItem>
        </CarouselContent>

        <div
          class="flex gap-4 absolute -bottom-10 sm:-bottom-8 left-1/2 -translate-x-1/2 px-4 sm:px-14"
        >
          <CarouselPrevious
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-white hover:bg-gray-200 hover:text-deep-blue border-none"
          />
          <CarouselNext
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-white hover:bg-gray-200 hover:text-deep-blue border-none"
          />
        </div>
      </Carousel>
    </div>
  </div>
</template>
