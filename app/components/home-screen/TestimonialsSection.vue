<script setup lang="ts">
import { ref } from 'vue';
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from '@/components/ui/carousel';
import { Star } from 'lucide-vue-next';

const testimonials = ref([
  {
    id: 1,
    name: 'Thomas Daniel',
    image: '/images/home/client1.svg',
    rating: 5,
    text: 'Phosfluorescently synergize covalent outsourcing through functional strategic theme areas. Assertively scale strategic portals without distinctive relationships. Holisticly cultivate tactical e-services before fully researched sources.',
  },
  {
    id: 2,
    name: 'Alena Alex',
    image: '/images/home/client2.svg',
    rating: 5,
    text: 'Phosfluorescently synergize covalent outsourcing through functional strategic theme areas. Assertively scale strategic portals without distinctive relationships. Holisticly cultivate tactical e-services before fully researched sources.',
  },
  {
    id: 3,
    name: 'Thomas Edison',
    image: '/images/home/client3.svg',
    rating: 5,
    text: 'Phosfluorescently synergize covalent outsourcing through functional strategic theme areas. Assertively scale strategic portals without distinctive relationships. Holisticly cultivate tactical e-services before fully researched sources.',
  },
  {
    id: 4,
    name: 'Jacob Jones',
    image: '/images/home/client4.svg',
    rating: 5,
    text: 'Phosfluorescently synergize covalent outsourcing through functional strategic theme areas. Assertively scale strategic portals without distinctive relationships. Holisticly cultivate tactical e-services before fully researched sources.',
  },
]);
</script>

<template>
  <div
    class="w-full flex flex-col text-center items-center justify-center py-16 sm:py-20 md:py-24 lg:py-32 bg-white"
  >
    <!-- Title -->
    <div
      class="font-semibold text-3xl sm:text-4xl md:text-5xl text-deep-blue mb-5 px-4"
    >
      <h2>Our Happy Clients</h2>
    </div>

    <p class="text-gray-600 text-base lg:text-lg leading-relaxed px-4 mb-12">
      We use only the best quality materials on the market in order to
      <br class="hidden sm:block" />
      provide the best products to our patients.
    </p>

    <!-- Carousel -->
    <div class="w-full max-w-7xl px-4 sm:px-6 lg:px-8">
      <Carousel>
        <CarouselContent class="-ml-3 mb-10">
          <CarouselItem
            v-for="testimonial in testimonials"
            :key="testimonial.id"
            class="pl-3 md:basis-1/2 lg:basis-1/3"
          >
            <div
              class="bg-gray-50 rounded-2xl p-6 sm:p-7 flex flex-col h-full border border-gray-100"
            >
              <!-- Header: Photo & Name -->
              <div class="flex items-center gap-4 mb-4">
                <img
                  :src="testimonial.image"
                  :alt="testimonial.name"
                  class="w-14 h-14 sm:w-16 sm:h-16 rounded-full object-cover flex-shrink-0"
                />
                <div class="text-left flex-1">
                  <h3
                    class="text-gray-900 font-semibold text-base sm:text-lg mb-1"
                  >
                    {{ testimonial.name }}
                  </h3>
                  <!-- Rating Stars -->
                  <div class="flex gap-0.5">
                    <Star
                      v-for="star in testimonial.rating"
                      :key="star"
                      class="w-4 h-4 fill-amber-400 text-amber-400"
                    />
                  </div>
                </div>
              </div>

              <!-- Testimonial Text -->
              <p
                class="text-gray-600 text-sm sm:text-base text-left leading-relaxed"
              >
                {{ testimonial.text }}
              </p>
            </div>
          </CarouselItem>
        </CarouselContent>

        <div
          class="flex gap-4 absolute -bottom-10 sm:-bottom-8 left-1/2 -translate-x-1/2 px-4 sm:px-14"
        >
          <CarouselPrevious
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-deep-blue hover:bg-gray-400 hover:text-deep-blue text-white border-none"
          />
          <CarouselNext
            class="inline-flex items-center justify-center w-20 h-10 sm:w-24 sm:h-11 rounded-none bg-deep-blue hover:bg-gray-400 hover:text-deep-blue text-white border-none"
          />
        </div>
      </Carousel>
    </div>
  </div>
</template>
