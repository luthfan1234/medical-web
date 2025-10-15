<script setup lang="ts">
import { ref } from 'vue';
import { Card, CardTitle, CardDescription } from '@/components/ui/card';

const articles = ref([
  {
    id: 1,
    image: '/images/article/article1.png',
    category: 'Self Care',
    title: 'The Importance of Regular Dental Check-ups',
    description:
      'Regular dental check-ups are essential for maintaining good oral health. They allow for the early detection of potential issues and ensure that your teeth and gums are in optimal condition.',
  },
  {
    id: 2,
    image: '/images/article/article2.png',
    category: 'Self Care',
    title: 'How to Prevent Cavities and Tooth Decay',
    description:
      'Learn the best practices for preventing cavities and maintaining healthy teeth through proper brushing, flossing, and dietary choices.',
  },
  {
    id: 3,
    image: '/images/article/article3.png',
    category: 'Self Care',
    title: 'Understanding Root Canal Treatment',
    description:
      'Root canal treatment can save your natural tooth and prevent further complications. Discover what to expect during this common dental procedure.',
  },
  {
    id: 4,
    image: '/images/article/article4.png',
    category: 'Self Care',
    title: 'Teeth Whitening: What You Need to Know',
    description:
      'Explore different teeth whitening options and learn how to achieve a brighter, more confident smile safely and effectively.',
  },
  {
    id: 5,
    image: '/images/article/article5.png',
    category: 'Self Care',
    title: 'Braces vs Invisalign: Which is Right for You?',
    description:
      'Compare traditional braces with Invisalign clear aligners to determine the best orthodontic treatment for your specific needs.',
  },
  {
    id: 6,
    image: '/images/article/article6.png',
    category: 'Self Care',
    title: 'Teaching Kids Good Dental Habits',
    description:
      'Start your children on the path to lifelong oral health with these fun and effective tips for establishing good dental hygiene habits.',
  },
  {
    id: 7,
    image: '/images/article/article7.png',
    category: 'Self Care',
    title: 'What to Do in a Dental Emergency',
    description:
      'Know how to respond quickly and effectively to common dental emergencies like knocked-out teeth, severe pain, or broken restorations.',
  },
  {
    id: 8,
    image: '/images/article/article8.png',
    category: 'Self Care',
    title: 'The Connection Between Oral and Overall Health',
    description:
      'Discover how your oral health affects your overall wellbeing and why maintaining healthy teeth and gums is crucial for your body.',
  },
]);
</script>

<template>
  <div class="py-26 ">
    <h2
      class="font-semibold text-3xl sm:text-4xl md:text-5xl text-deep-blue mb-5"
    >
      Articles
    </h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <Card
        v-for="article in articles"
        :key="article.id"
        class="p-5 border-none shadow-none bg-soft-blue"
      >
        <div class="mb-4">
          <img
            :src="article.image"
            :alt="article.title"
            class="w-full h-48 object-cover rounded-xl"
          />
        </div>
        <button class="w-24 h-9 bg-deep-blue text-white rounded-lg">
          {{ article.category }}
        </button>
        <CardTitle class="font-medium text-deep-blue text-lg">
          {{ article.title }}
        </CardTitle>
        <CardDescription class="text-gray-600 text-sm">
          {{ article.description }}
        </CardDescription>
      </Card>
    </div>
    <button
      class="w-full flex items-center mt-10 justify-center sm:w-auto px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue transition whitespace-nowrap mx-auto"
    >
      Check out more
    </button>
  </div>
</template>
