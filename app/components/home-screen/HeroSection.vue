<script setup>
import ServicesSection from '~/components/home-screen/ServicesSection.vue';
</script>

<template>
  <div
    class="relative flex flex-col lg:flex-row items-center mt-8 md:mt-12 lg:mt-16 mb-12"
  >
    <div class="relative z-10 text-left w-full mt-8 lg:mt-0">
      <h1
        class="text-deep-blue font-semibold text-3xl sm:text-4xl md:text-5xl lg:text-6xl leading-tight mb-4 lg:mb-5"
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
      <div class="flex flex-col sm:flex-row items-center justify-start space-y-4 sm:space-y-0 sm:space-x-6 mb-8 lg:mb-12">
        <button
          class="w-full sm:w-auto btn btn-primary px-5 py-3 md:px-6 lg:px-7 md:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue hover:text-white"
        >
          Book an appointment
        </button>

        <div class="flex flex-row space-x-4 xs:flex-row items-center xs:space-x-3.5">
          <button class="btn rounded-lg outline-2 outline-bright-blue flex flex-shrink-0">
            <img
              src="/icon/icon-phone-home.svg"
              alt="Booking"
              class="h-12 w-12 md:h-14 md:w-14 p-2"
            />
          </button>
          <div class="text-left">
            <p class="text-bright-blue font-semibold leading-tight mb-1 text-sm md:text-base">
              Dental 24H Emergency
            </p>
            <p class="text-primary text-xs md:text-sm font-medium">
              0900-78601
            </p>
          </div>
        </div>
      </div>

      <!-- Testimonial Card -->
      <div
        class="w-full max-w-md sm:max-w-sm lg:max-w-96 bg-white rounded-2xl shadow-md p-4 lg:p-5 flex flex-col gap-3 sm:ml-0"
      >
        <div class="flex items-start justify-between">
          <div class="flex items-center gap-3">
            <img
              src="/images/person-thomas.svg"
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
            src="/icon/icon-linkedin.svg"
            alt="LinkedIn"
            class="w-4 h-4 lg:w-5 lg:h-5 flex-shrink-0 mt-1"
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
      class="relative lg:absolute lg:right-0 w-full lg:w-1/2 flex justify-center lg:justify-end items-center mt-8 sm:mt-12 lg:mt-0"
    >
      <img
        src="/images/people.svg"
        alt="Hero Section"
        class="w-full max-w-xs sm:max-w-sm md:max-w-md lg:max-w-full object-contain"
      />
    </div>
  </div>
  <ServicesSection />
</template>
