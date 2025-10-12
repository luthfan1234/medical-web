<template>
  <div class="relative flex items-center">
    <div class="relative z-10 py-45">
      <h1 class="text-deep-blue text-6xl font-weight-600 font-semibold mb-5">
        Get Ready For Your Best <br />
        Ever Dental Experience!
      </h1>
      <p class="text-lg mb-6 text-deep-blue font-regular">
        We use only the best quality materials on the market in order to <br />
        provide the best products to our patients, So don't worry about
        <br />anything and book yourself.
      </p>
      <div class="flex items-center space-x-7">
        <button
          class="btn btn-primary px-7 py-4 bg-bright-blue text-white rounded-lg font-semibold"
        >
          Book an appointment
        </button>
        <div class="flex justify-center items-center space-x-3.5">
          <button class="btn rounded-lg outline-2 outline-bright-blue">
            <img
              src="@/assets/icon/icon-phone-home.svg"
              alt="Booking"
              class="h-14 w-14 p-2"
            />
          </button>
          <div class="text-left">
            <p class="text-bright-blue font-semibold leading-tight mb-1">
              Dental 24H Emergency
            </p>
            <p class="text-primary text-sm font-medium">0900-78601</p>
          </div>
        </div>
      </div>
      <div
        class="w-96 h-28 mt-12 bg-background rounded-2xl shadow-lg flex items-center justify-center"
      >
        <div class="flex items-start justify-between">
          <div class="flex items-center gap-3">
            <img
              src="@/assets/images/person-thomas.svg"
              alt="Thomas Daniel"
              class="w-12 h-12 rounded-full object-cover"
            />
            <div>
              <h3 class="text-gray-900 font-semibold text-base">
                Thomas Daniel
              </h3>
              <p class="text-gray-500 text-sm">Sr Dental</p>
            </div>
          </div>
          <img
            src="@/assets/icon/linkedin-icon.svg"
            alt="LinkedIn"
            class="w-5 h-5"
          />
        </div>

        <!-- Bagian isi testimonial -->
        <p class="text-gray-600 text-sm leading-snug">
          Top quality dental treatment done by field experts, highly recommended
          for everyone.
        </p>
      </div>
    </div>
    <div class="absolute justify-end right-0 flex items-center">
      <img
        src="@/assets/images/people.svg"
        alt="Hero Section"
        class="w-full md:w-3/4 lg:w-[45rem] h-auto object-contain mx-auto"
      />
    </div>
  </div>
</template>
