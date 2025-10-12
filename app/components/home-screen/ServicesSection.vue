<script setup lang="ts">
import Card from '@/components/ui/card/Card.vue';
import CardTitle from '@/components/ui/card/CardTitle.vue';
import CardDescription from '@/components/ui/card/CardDescription.vue';
</script>

<template>
  <div class="bg-soft-blue py-12">
    <div class="flex items-center justify-center">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 px-12 gap-12">
        <!-- Service 1 -->
        <Card
          class="mx-auto w-96 h-72 bg-white rounded-2xl flex items-center justify-center shadow-none border-none"
        >
          <div class="flex justify-center items-center w-16 h-16 mt-4">
            <img
              src="@/assets/icon/teeth.svg"
              alt="Tooth Icon"
              class="w-16 h-16"
            />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue">
            Root Canal Treatment
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed px-6 flex items-center justify-center text-center"
          >
            Root canal treatment (endodontics) is <br />
            a dental procedure used to treat <br />infection at the centre of a
            tooth.
          </CardDescription>
          <button
            class="mb-4 text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:arrow-right" class="w-4 h-4" />
          </button>
        </Card>
        <!-- Service 2 -->
        <Card
          class="mx-auto w-96 h-72 bg-white rounded-2xl flex items-center justify-center shadow-none border-none"
        >
          <div class="flex justify-center items-center w-16 h-16 mt-4">
            <img
              src="@/assets/icon/mouth.svg"
              alt="Tooth Icon"
              class="w-16 h-16"
            />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue">
            Cosmetic Dentist
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed px-6 flex items-center justify-center text-center"
          >
            Cosmetic dentistry is the branch of <br />
            dentistry that focuses on improving <br />
            the appearance of your smile.
          </CardDescription>
          <button
            class="mb-4 text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:arrow-right" class="w-4 h-4" />
          </button>
        </Card>
        <!-- Service 3 -->
        <Card
          class="mx-auto w-96 h-72 bg-white rounded-2xl flex items-center justify-center shadow-none border-none"
        >
          <div class="flex justify-center items-center w-16 h-16 mt-4">
            <img
              src="@/assets/icon/implant.svg"
              alt="Tooth Icon"
              class="w-16 h-16"
            />
          </div>
          <CardTitle class="text-lg font-semibold text-deep-blue">
            Dental Implants
          </CardTitle>
          <CardDescription
            class="text-primary text-md font-regular leading-relaxed px-6 flex items-center justify-center text-center"
          >
            A dental implant is an artificial tooth root <br />
            that's placed into your jaw to hold <br />
            a prosthetic tooth or bridge.
          </CardDescription>
          <button
            class="mb-4 text-primary font-medium flex items-center justify-center gap-2 hover:underline"
          >
            <span>Learn More</span>
            <Icon name="lucide:circle-arrow-right" class="w-4 h-4" />
          </button>
        </Card>
      </div>
    </div>
  </div>
</template>
