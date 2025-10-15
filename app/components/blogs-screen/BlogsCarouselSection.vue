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
    category: 'Self Care',
    writer: '~Anita Jackson',
    title: 'Care of your Teeth',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
  {
    id: 2,
    category: 'Self Care',
    writer: '~Anita Jackson',
    title: 'Care of your Teeth',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
  {
    id: 3,
    category: 'Self Care',
    writer: '~Anita Jackson',
    title: 'Care of your Teeth',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
  {
    id: 4,
    category: 'Self Care',
    title: 'Care of your Teeth',
    writer: '~Anita Jackson',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
  {
    id: 5,
    category: 'Self Care',
    title: 'Care of your Teeth',
    writer: '~Anita Jackson',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
  {
    id: 6,
    category: 'Self Care',
    title: 'Care of your Teeth',
    writer: '~Anita Jackson',
    description: ' Lorem ipsum dolor sit amet consectetur.',
    image: '/images/article/article6.png',
    link: '#',
  },
]);
</script>

<template>
  <div class="w-full flex flex-col">
    <div class="">
      <Carousel>
        <CarouselContent class="-ml-3 bg">
          <CarouselItem
            v-for="blog in blogs"
            :key="blog.id"
            class="pl-3 md:basis-1/2 lg:basis-1/3 xl:basis-1/4"
          >
            <div
              class="relative rounded-xl overflow-hidden bg-soft-blue w-full h-[31rem] flex flex-col px-5 py-6"
            >
              <div class="">
                <img
                  :src="blog.image"
                  :alt="blog.title"
                  class="w-full h-full object-cover"
                />
              </div>
              <div class="flex justify-between items-center">
                <button
                  class="w-24 h-9 bg-deep-blue text-white rounded-lg items-start"
                >
                  {{ blog.category }}
                </button>
                <p class="text-sm text-gray-500 mt-1">{{ blog.writer }}</p>
              </div>

              <div>
                <CardTitle class="font-medium text-deep-blue text-lg text-left">
                  {{ blog.title }}
                </CardTitle>
                <CardDescription class="text-gray-600 text-sm text-left">
                  {{ blog.description }}
                </CardDescription>
              </div>
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
