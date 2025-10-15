<template>
  <div class="pb-10">
    <nav
      class="flex items-center justify-between px-4 md:px-10 py-1 bg-white text-deep-blue font-size-16 font-medium text-center rounded-2xl"
    >
      <!-- Logo -->
      <RouterLink to="/">
        <img
          src="/images/logo.svg"
          class="w-16 h-16 md:w-24 md:h-24 hover:scale-105 transition-transform duration-200"
          alt="todo list logo"
        />
      </RouterLink>

      <!-- Desktop Navigation Links -->
      <div class="hidden md:flex items-center space-x-8">
        <RouterLink
          to="/"
          class="btn btn-primary hover:font-semibold transition-all duration-200"
          :class="{ 'font-semibold': isActiveRoute('/') }"
        >
          Home
        </RouterLink>
        <RouterLink
          to="/services"
          class="btn btn-primary hover:font-semibold transition-all duration-200"
          :class="{ 'font-semibold': isActiveRoute('services') }"
        >
          Services
        </RouterLink>
        <RouterLink
          to="/blogs"
          class="btn btn-primary hover:font-semibold transition-all duration-200"
          :class="{ 'font-semibold': isActiveRoute('blogs') }"
        >
          Blogs
        </RouterLink>
        <RouterLink
          to="/about"
          class="btn btn-primary hover:font-semibold transition-all duration-200"
          :class="{ 'font-semibold': isActiveRoute('about') }"
        >
          About
        </RouterLink>
        <RouterLink
          to="/contact"
          class="btn btn-primary hover:font-semibold transition-all duration-200"
          :class="{ 'font-semibold': isActiveRoute('contact') }"
        >
          Contact
        </RouterLink>
      </div>

      <!-- Desktop Right Side -->
      <div class="hidden md:flex items-center space-x-5">
        <div
          class="h-8 w-8 flex items-center justify-center rounded-full bg-primary text-white hover:bg-deep-blue hover:scale-110 transition-transform duration-200 cursor-pointer"
        >
          <i class="fa fa-user-circle" />
        </div>
        <RouterLink
          to="/booking"
          class="btn btn-primary px-7 py-3.5 bg-bright-blue rounded-lg font-semibold text-white hover:bg-deep-blue hover:scale-105 transition-all duration-200"
        >
          Book Now
        </RouterLink>
      </div>

      <!-- Mobile Menu Button -->
      <button
        @click="toggleMobileMenu"
        class="md:hidden flex items-center justify-center w-8 h-8 text-deep-blue hover:bg-deep-blue hover:text-white rounded-lg transition-all duration-200"
        aria-label="Toggle menu"
      >
        <Icon name="heroicons:bars-3" class="w-6 h-6" />
      </button>
    </nav>

    <!-- Mobile Menu Overlay -->
    <div
      v-if="isMobileMenuOpen"
      class="md:hidden fixed inset-0 bg-black bg-opacity-50 z-40"
      @click="closeMobileMenu"
    />

    <!-- Mobile Menu -->
    <div
      :class="[
        'md:hidden fixed top-0 right-0 h-full w-64 bg-soft-blue transform transition-transform duration-300 ease-in-out z-50',
        isMobileMenuOpen ? 'translate-x-0' : 'translate-x-full',
      ]"
    >
      <div class="flex flex-col p-6">
        <!-- Close Button -->
        <button
          @click="closeMobileMenu"
          class="self-end mb-8 w-8 h-8 flex items-center justify-center text-deep-blue hover:bg-deep-blue hover:text-white rounded-lg transition-all duration-200"
          aria-label="Close menu"
        >
          <Icon name="heroicons:x-mark" class="w-6 h-6" />
        </button>

        <!-- Mobile Navigation Links -->
        <div class="flex flex-col space-y-6">
          <RouterLink
            to="/"
            class="btn btn-primary text-left hover:pl-4 hover:font-semibold transition-all duration-200"
            @click="closeMobileMenu"
            :class="{ 'font-semibold': isActiveRoute('/') }"
          >
            Home
          </RouterLink>
          <RouterLink
            to="/services"
            class="btn btn-primary text-left hover:pl-4 hover:font-semibold transition-all duration-200"
            @click="closeMobileMenu"
            :class="{ 'font-semibold': isActiveRoute('services') }"
          >
            Services
          </RouterLink>
          <RouterLink
            to="/blogs"
            class="btn btn-primary text-left hover:pl-4 hover:font-semibold transition-all duration-200"
            @click="closeMobileMenu"
            :class="{ 'font-semibold': isActiveRoute('blogs') }"
          >
            Blogs
          </RouterLink>
          <RouterLink
            to="/about"
            class="btn btn-primary text-left hover:pl-4 hover:font-semibold transition-all duration-200"
            @click="closeMobileMenu"
            :class="{ 'font-semibold': isActiveRoute('about') }"
          >
            About
          </RouterLink>
          <RouterLink
            to="/contact"
            class="btn btn-primary text-left hover:pl-4 hover:font-semibold transition-all duration-200"
            @click="closeMobileMenu"
            :class="{ 'font-semibold': isActiveRoute('contact') }"
          >
            Contact
          </RouterLink>
        </div>

        <!-- Mobile User & Book Button -->
        <div class="mt-8 pt-6 border-t border-deep-blue/20">
          <div
            class="flex items-center space-x-3 mb-4 hover:bg-deep-blue/10 p-2 rounded-lg transition-colors duration-200 cursor-pointer"
          >
            <div
              class="h-8 w-8 flex items-center justify-center rounded-full bg-primary text-white hover:scale-110 transition-transform duration-200"
            >
              <i class="fa fa-user-circle" />
            </div>
            <span class="text-deep-blue">Profile</span>
          </div>
          <RouterLink
            to="/booking"
            class="btn btn-primary w-full px-4 py-3 bg-bright-blue rounded-lg font-semibold text-white text-center block hover:bg-deep-blue hover:scale-105 transition-all duration-200"
            @click="closeMobileMenu"
          >
            Book Now
          </RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const route = useRoute();

const isMobileMenuOpen = ref(false);

const isActiveRoute = (path: string): boolean => {
  const currentPath = route.path === '/' ? '' : route.path.slice(1);
  return currentPath === path;
};

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false;
};

// Close mobile menu when route changes
watch(
  () => useRoute().path,
  () => {
    closeMobileMenu();
  }
);
</script>
