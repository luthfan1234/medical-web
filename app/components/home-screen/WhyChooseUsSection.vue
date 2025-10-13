<template>
  <div class="bg-soft-blue h-[32rem] flex flex-row items-center">
    <!-- Left Image -->
    <img class="px-28" src="/images/why-choose-us.png" alt="Why Choose Us " />

    <!-- Right Content -->
    <div class="flex-1">
      <h2 class="text-5xl font-semibold text-deep-blue text-left">
        Why choose Smile for all <br />
        your dental treatments?
      </h2>
      <p class="mt-5 text-lg text-deep-blue font-regular leading-relaxed">
        We use only the best quality materials on the market in order <br />to
        provide the best products to our patients.
      </p>
      <div class="bg-soft-blue mt-6 mb-8 rounded-xl">
        <ul class="space-y-4 text-deep-blue">
          <li class="flex items-center space-x-3">
            <Icon name="lucide:shield-check" class="w-5 h-5 text-bright-blue" />
            <span class="font-medium">Top quality dental team</span>
          </li>
          <li class="flex items-center space-x-3">
            <Icon name="lucide:shield-check" class="w-5 h-5 text-bright-blue " />
            <span class="font-medium">State of the art dental services</span>
          </li>
          <li class="flex items-center space-x-3">
            <Icon name="lucide:shield-check" class="w-5 h-5 text-bright-blue" />
            <span class="font-medium">Discount on all dental treatment</span>
          </li>
          <li class="flex items-center space-x-3">
            <Icon name="lucide:shield-check" class="w-5 h-5 text-bright-blue" />
            <span class="font-medium">Enrollment is quick and easy</span>
          </li>
        </ul>
      </div>
      <button
        class="w-fullsm:w-auto btn btn-primary px-6 lg:px-7 py-3 lg:py-4 bg-bright-blue text-white rounded-lg font-semibold hover:bg-deep-blue hover:text-white"
      >
        Book an appointment
      </button>
    </div>
  </div>
</template>
