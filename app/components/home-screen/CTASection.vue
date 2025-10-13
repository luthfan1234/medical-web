<template>
  <div class="px-20 py-36 flex flex-row items-center">
    <!-- Left content -->
    <div class="flex-1 flex flex-col">
      <div class="font-semibold text-5xl text-deep-blue text-left mb-2">
        <h2>
          Leave your worries at the <br />
          door and enjoy a healthier, <br />
          more precise smile
        </h2>
      </div>

      <div>
        <p
          class="text-base lg:text-lg mt-4 mb-8 text-deep-blue font-regular leading-relaxed"
        >
          We use only the best quality materials on the market in order to
          <br />
          provide the best products to our patients, So don’t worry about <br />
          anything and book yourself.
        </p>
        <button
          class="w-fullsm:w-auto btn btn-primary px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue hover:text-white"
        >
          Book an appointment
        </button>
      </div>
    </div>

    <!-- Right image -->
    <div class="relative w-[26rem] h-[22.5rem]">
      <!-- Background biru -->
      <div
        class="absolute bottom-6 left-6 w-full h-full bg-gradient-to-r from-soft-blue to-sky-blue rounded-2xl"
      ></div>

      <!-- Gambar utama -->
      <img
        src="/images/cta-images.png"
        alt="Happy patient"
        class="relative w-full h-full object-cover rounded-2xl"
      />
    </div>
  </div>
</template>
