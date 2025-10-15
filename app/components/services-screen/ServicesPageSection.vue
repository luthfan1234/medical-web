<script setup lang="ts">
import Card from '@/components/ui/card/Card.vue';
import CardTitle from '@/components/ui/card/CardTitle.vue';
import CardDescription from '@/components/ui/card/CardDescription.vue';
</script>

<template>
  <div class="bg-soft-blue py-16 sm:py-20 md:py-24">
    <div class="flex items-center justify-center">
      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8"
      >
        <!-- Service 1 -->
        <Card class="w-full p-6 sm:p-8 border-none shadow-none">
          <div class="flex justify-center items-center mb-4">
            <img src="/icon/teeth.svg" alt="Tooth Icon" class="w-16 h-16" />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue mb-2">
            Root Canal Treatment
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed mb-4"
          >
            Root canal treatment (endodontics) is a dental procedure used to
            treat infection at the centre of a tooth.
          </CardDescription>
          <button
            class="text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:circle-arrow-right" class="w-4 h-4" />
          </button>
        </Card>
        <!-- Service 2 -->
        <Card class="w-full p-6 sm:p-8 border-none shadow-none">
          <div class="flex justify-center items-center mb-4">
            <img src="/icon/mouth.svg" alt="Tooth Icon" class="w-16 h-16" />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue mb-2">
            Cosmetic Dentist
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed mb-4"
          >
            Cosmetic dentistry is the branch of dentistry that focuses on
            improving the appearance of your smile.
          </CardDescription>
          <button
            class="text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:circle-arrow-right" class="w-4 h-4" />
          </button>
        </Card>
        <!-- Service 3 -->
        <Card class="w-full p-6 sm:p-8 border-none shadow-none">
          <div class="flex justify-center items-center mb-4">
            <img src="/icon/implant.svg" alt="Tooth Icon" class="w-16 h-16" />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue mb-2">
            Dental Implants
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed mb-4"
          >
            A dental implant is an artificial tooth root that's placed into your
            jaw to hold a prosthetic tooth or bridge.
          </CardDescription>
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
