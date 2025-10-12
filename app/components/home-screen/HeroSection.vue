<script setup>
import ServicesSection from '~/components/home-screen/ServicesSection.vue';
</script>

<template>
  <div class="relative flex flex-col lg:flex-row items-center mt-18 mb-12">
    <div class="relative z-10 text-left w-full mt-8 lg:mt-0">
      <h1
        class="text-deep-blue font-semibold text-3xl sm:text-3xl md:text-5xl lg:text-6xl leading-tight mb-4 lg:mb-5"
      >
        Get Ready For Your Best <br class="hidden sm:block" />
        Ever Dental Experience!
      </h1>
      <p
        class="text-base lg:text-lg mb-6 text-deep-blue font-regular leading-relaxed"
      >
        We use only the best quality materials on the market in order to
        <br class="hidden lg:block" />
        provide the best products to our patients, So don't worry about
        <br class="hidden lg:block" />anything and book yourself.
      </p>

      <!-- Buttons Section -->
      <div
        class="flex flex-col sm:flex-row items-start sm:items-center space-y-4 sm:space-y-0 sm:space-x-7 mb-8 lg:mb-12"
      >
        <button
          class="w-full sm:w-auto btn btn-primary px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold"
        >
          Book an appointment
        </button>

        <div class="flex items-center space-x-3 lg:space-x-3.5">
          <button
            class="btn rounded-lg outline-2 outline-bright-blue flex-shrink-0"
          >
            <img
              src="@/assets/icon/icon-phone-home.svg"
              alt="Booking"
              class="h-12 w-12 lg:h-14 lg:w-14 p-2"
            />
          </button>
          <div class="text-left">
            <p
              class="text-bright-blue font-semibold leading-tight mb-1 text-sm lg:text-base"
            >
              Dental 24H Emergency
            </p>
            <p class="text-primary text-xs lg:text-sm font-medium">
              0900-78601
            </p>
          </div>
        </div>
      </div>

      <!-- Testimonial Card -->
      <div
        class="w-full max-w-sm lg:max-w-96 bg-white rounded-2xl shadow-md p-4 lg:p-5 flex flex-col gap-3"
      >
        <div class="flex items-start justify-between">
          <div class="flex items-center gap-3">
            <img
              src="@/assets/images/person-thomas.svg"
              alt="Thomas Daniel"
              class="w-10 h-10 lg:w-12 lg:h-12 rounded-full object-cover flex-shrink-0"
            />
            <div>
              <h3 class="text-primary font-semibold text-sm lg:text-base">
                Thomas Daniel
              </h3>
              <p class="text-primary text-xs lg:text-sm">Sr Dental</p>
            </div>
          </div>
          <img
            src="@/assets/icon/icon-linkedin.svg"
            alt="LinkedIn"
            class="w-4 h-4 lg:w-5 lg:h-5 flex-shrink-0"
          />
        </div>

        <p class="text-primary text-xs lg:text-sm leading-snug">
          Top quality dental treatment done by field experts, highly recommended
          for everyone.
        </p>
      </div>
    </div>

    <!-- Hero Image -->
    <div
      class="relative lg:absolute lg:right-0 w-full lg:w-1/2 flex justify-center lg:justify-end items-center mt-8 lg:mt-0"
    >
      <img
        src="@/assets/images/people.svg"
        alt="Hero Section"
        class="w-full max-w-md sm:max-w-lg lg:max-w-none lg:w-full lg:h-auto object-contain"
      />
    </div>
  </div>
  <ServicesSection />
</template>
