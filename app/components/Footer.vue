<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="px-4 sm:px-6 lg:px-8">
    <!-- Top section with logo and navigation -->
    <div class="flex flex-col sm:flex-row items-center justify-between gap-4 sm:gap-0">
      <RouterLink to="/" class="flex-shrink-0">
        <img
          src="@/assets/images/logo.svg"
          class="w-16 h-16 sm:w-20 sm:h-20 lg:w-24 lg:h-24"
          alt="todo list logo"
        />
      </RouterLink>
      
      <!-- Navigation links -->
      <div class="flex flex-wrap items-center justify-center sm:justify-end text-deep-blue gap-2 sm:gap-4 lg:gap-8">
        <RouterLink to="/create" class="btn btn-primary text-sm sm:text-base">Home</RouterLink>
        <RouterLink to="/create" class="btn btn-primary text-sm sm:text-base">Services</RouterLink>
        <RouterLink to="/create" class="btn btn-primary text-sm sm:text-base">Blogs</RouterLink>
        <RouterLink to="/create" class="btn btn-primary text-sm sm:text-base">About</RouterLink>
        <RouterLink to="/create" class="btn btn-primary text-sm sm:text-base">Contact</RouterLink>
      </div>
    </div>
    
    <!-- Divider -->
    <hr class="my-4 sm:my-6 border-t-4 border-deep-blue" />
    
    <!-- Bottom section with copyright and social links -->
    <div class="flex flex-col sm:flex-row items-center justify-between gap-4 sm:gap-0">
      <!-- Copyright text -->
      <p class="text-gray-600 dark:text-gray-400 text-xs sm:text-sm text-center sm:text-left order-2 sm:order-1">
        &copy; {{ new Date().getFullYear() }} All rights reserved ® uifry.com | Terms and conditions apply!
      </p>
      
      <!-- Social media icons -->
      <div class="flex items-center gap-2 sm:gap-4 order-1 sm:order-2">
        <a href="#" class="hover:opacity-80 transition-opacity">
          <img
            src="@/assets/icon/facebook.svg"
            alt="Facebook"
            class="w-6 h-6 sm:w-7 sm:h-7 lg:w-8 lg:h-8"
          />
        </a>
        <a href="#" class="hover:opacity-80 transition-opacity">
          <img
            src="@/assets/icon/instagram.svg"
            alt="Instagram"
            class="w-6 h-6 sm:w-7 sm:h-7 lg:w-8 lg:h-8"
          />
        </a>
        <a href="#" class="hover:opacity-80 transition-opacity">
          <img 
            src="@/assets/icon/youtube.svg" 
            alt="YouTube" 
            class="w-6 h-6 sm:w-7 sm:h-7 lg:w-8 lg:h-8" 
          />
        </a>
        <a href="#" class="hover:opacity-80 transition-opacity">
          <img
            src="@/assets/icon/linkedin.svg"
            alt="LinkedIn"
            class="w-6 h-6 sm:w-7 sm:h-7 lg:w-8 lg:h-8"
          />
        </a>
        <a href="#" class="hover:opacity-80 transition-opacity">
          <img 
            src="@/assets/icon/twitter.svg" 
            alt="Twitter" 
            class="w-6 h-6 sm:w-7 sm:h-7 lg:w-8 lg:h-8" 
          />
        </a>
      </div>
    </div>
  </div>
</template>
