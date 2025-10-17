<script setup lang="ts">
import { ref } from 'vue';

const doctorSpecialists = ref([
  {
    id: 1,
    name: 'DR. Brent',
    specialty: 'Speciality in General & Cosmetic Service',
    image: '/images/about/specialists/specialists1.png',
    description: `Dr. Brent provides general and cosmetic dentistry services at Northern
      Heights Dental in Flagstaff, Arizona. He has extensive experience in general and
      cosmetic dentistry, including full mouth restoration, dental veneers, crowns, bridges,
      dental implants, wisdom teeth extractions, Invisalign, and dentures. Dr. Brent and his
      younger sister grew up in Massachusetts with a mother who worked as a hygienist and a
      grandfather who was a general dentist.`,
  },
]);
</script>

<template>
  <div class="flex flex-col items-center justify-center mb-20 mt-20">
    <h1 class="font-semibold text-6xl text-deep-blue mb-5">
      Meet our specialists
    </h1>
    <p>
      We use only the best quality materials on the market in <br />
      order to provide the best products to our patients.
    </p>
  </div>

  <div
    v-if="doctorSpecialists[0]"
    class="flex items-center space-x-8 justify-center px-20"
  >
    <div class="flex-shrink-0">
      <img :src="doctorSpecialists[0].image" class="w-full max-w-md mb-5" />
    </div>

    <div class="flex flex-col space-y-4 items-start">
      <h1 class="font-semibold text-2xl text-deep-blue">
        {{ doctorSpecialists[0].name }}
        <span class="font-normal text-lg">
          {{ doctorSpecialists[0].specialty }}
        </span>
      </h1>
      <p class="text-lg leading-relaxed">
        {{ doctorSpecialists[0].description }}
      </p>
      <button
        class="mt-4 sm:w-auto px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue transition whitespace-nowrap"
      >
        Check out more
      </button>
    </div>
  </div>
</template>
