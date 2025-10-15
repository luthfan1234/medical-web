<template>
  <div class="px-20 py-36 flex flex-row items-center">
    <!-- Left content -->
    <div class="flex-1 flex flex-col">
      <div class="font-semibold text-5xl text-deep-blue text-left mb-2">
        <h2>
          We're welcoming new <br /> patients and can't wait <br />
          to meet you.
        </h2>
      </div>

      <div>
        <p
          class="text-base lg:text-lg mt-4 text-deep-blue font-regular leading-relaxed"
        >
          We use only the best quality materials on the market in order to
          <br />
          provide the best products to our patients, So don't worry about <br />
          anything and book yourself.
        </p>
      </div>

      <div
        class="flex items-center w-full max-w-md mt-10 rounded-lg overflow-hidden border border-gray-300 bg-white"
      >
        <div class="flex items-center justify-center pl-4">
          <Icon name="lucide:phone" class="w-4 h-4 text-muted-foreground" />
        </div>
        <input
          type="text"
          placeholder="Enter your Phone Number"
          class="flex-grow px-3 py-3 text-muted-foreground placeholder-muted-foreground focus:outline-none"
        />
        <button
          class="bg-bright-blue text-white font-semibold px-5 py-3 hover:bg-deep-blue transition-all duration-200"
        >
          Submit
        </button>
      </div>
    </div>
    <div class="relative w-[26rem] h-[22.5rem]">
      <div
        class="absolute bottom-6 left-6 w-full h-full bg-gradient-to-r from-soft-blue to-sky-blue rounded-2xl"
      ></div>
      <img
        src="/images/home/patient.png"
        alt="Happy patient"
        class="relative w-full h-full object-cover rounded-2xl"
      />
    </div>
  </div>
</template>
