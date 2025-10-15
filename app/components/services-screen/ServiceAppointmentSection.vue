<template>
  <div
    class="w-full bg-deep-blue text-white py-20 px-10 md:px-24 flex justify-center"
  >
    <div
      class="flex flex-col lg:flex-row items-center justify-between w-full max-w-6xl gap-12"
    >
      <!-- Kiri: Text Section -->
      <div class="flex flex-col max-w-xl">
        <h1 class="font-semibold text-4xl leading-snug mb-6">
          Leave Your Worries At The Door And Enjoy A Healthier, More Precise
          Smile
        </h1>

        <p class="text-lg text-gray-200 mb-8 leading-relaxed">
          We use only the best quality materials on the market in order to
          provide the best products to our patients, so don’t worry about
          anything and book yourself.
        </p>

        <button
          class="w-44 px-6 py-3 bg-bright-blue text-white rounded-lg font-semibold hover:bg-blue-500 flex items-center justify-center gap-2"
        >
          Learn More
          <Icon name="lucide:circle-arrow-right" class="w-4 h-4" />
        </button>
      </div>

      <!-- Kanan: Form Section -->
      <Card class="bg-white shadow-lg rounded-xl w-full max-w-sm p-8">
        <CardHeader>
          <CardTitle
            class="text-xl font-semibold text-gray-800 text-center mb-6"
          >
            Request Appointment
          </CardTitle>
        </CardHeader>
        <CardContent class="space-y-5">
          <input
            type="text"
            placeholder="Full Name"
            class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-bright-blue"
          />
          <input
            type="text"
            placeholder="Phone Number"
            class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-bright-blue"
          />
          <input
            type="email"
            placeholder="Email Address"
            class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-bright-blue"
          />
          <button
            class="w-full py-2 bg-bright-blue text-white rounded-md font-semibold hover:bg-deep-blue transition"
          >
            Submit
          </button>
        </CardContent>
      </Card>
    </div>
  </div>
</template>
