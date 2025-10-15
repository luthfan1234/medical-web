<template>
  <div
    class="px-4 sm:px-8 md:px-12 lg:px-20 py-16 sm:py-20 md:py-24 lg:py-36 flex flex-col lg:flex-row items-center gap-12 lg:gap-16"
  >
    <!-- Left content -->
    <div
      class="flex-1 flex flex-col text-center lg:text-left items-center lg:items-start"
    >
      <div
        class="font-semibold text-3xl sm:text-4xl md:text-5xl text-deep-blue mb-2"
      >
        <h2>
          Leave your worries at the <br class="hidden md:block" />
          door and enjoy a healthier, <br class="hidden md:block" />
          more precise smile
        </h2>
      </div>

      <div>
        <p
          class="text-base lg:text-lg mt-4 mb-8 text-deep-blue font-regular leading-relaxed"
        >
          We use only the best quality materials on the market in order to
          <br class="hidden lg:block" />
          provide the best products to our patients, So don’t worry about
          <br class="hidden lg:block" />
          anything and book yourself.
        </p>
        <button
          class="w-full sm:w-auto btn btn-primary px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue hover:text-white"
        >
          Book an appointment
        </button>
      </div>
    </div>

    <!-- Right image -->
    <div
      class="relative w-full max-w-md lg:max-w-lg h-auto lg:w-[26rem] lg:h-[22.5rem]"
    >
      <!-- Background biru -->
      <div
        class="absolute bottom-4 left-4 sm:bottom-6 sm:left-6 w-full h-full bg-gradient-to-r from-soft-blue to-sky-blue rounded-2xl"
      ></div>

      <!-- Gambar utama -->
      <img
        src="/images/home/cta-images.png"
        alt="Happy patient"
        class="relative w-full h-full object-cover rounded-2xl"
      />
    </div>
  </div>
</template>
