<template>
  <div class="pb-10">
    <nav
      class="flex items-center justify-between px-4 md:px-10 py-1 bg-soft-blue text-deep-blue font-size-16 font-medium text-center rounded-2xl"
    >
      <!-- Logo -->
      <RouterLink to="/">
        <img
          src="@/assets/images/logo.svg"
          class="w-16 h-16 md:w-24 md:h-24"
          alt="todo list logo"
        />
      </RouterLink>

      <!-- Desktop Navigation Links -->
      <div class="hidden md:flex items-center space-x-8">
        <RouterLink to="/" class="btn btn-primary">Home</RouterLink>
        <RouterLink to="/services" class="btn btn-primary">Services</RouterLink>
        <RouterLink to="/blogs" class="btn btn-primary">Blogs</RouterLink>
        <RouterLink to="/about" class="btn btn-primary">About</RouterLink>
        <RouterLink to="/contact" class="btn btn-primary">Contact</RouterLink>
      </div>

      <!-- Desktop Right Side -->
      <div class="hidden md:flex items-center space-x-5">
        <div
          class="h-8 w-8 flex items-center justify-center rounded-full bg-primary text-white"
        >
          <i class="fa fa-user-circle" />
        </div>
        <RouterLink
          to="/booking"
          class="btn btn-primary px-7 py-3.5 bg-bright-blue rounded-lg font-semibold text-white"
        >
          Book Now
        </RouterLink>
      </div>

      <!-- Mobile Menu Button -->
      <button
        @click="toggleMobileMenu"
        class="md:hidden flex items-center justify-center w-8 h-8 text-deep-blue"
        aria-label="Toggle menu"
      >
        <Icon name="lucide:menu" class="w-6 h-6" />
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
        isMobileMenuOpen ? 'translate-x-0' : 'translate-x-full'
      ]"
    >
      <div class="flex flex-col p-6">
        <!-- Close Button -->
        <button
          @click="closeMobileMenu"
          class="self-end mb-8 w-8 h-8 flex items-center justify-center text-deep-blue"
          aria-label="Close menu"
        >
          <Icon name="lucide:x" class="w-6 h-6" />
        </button>

        <!-- Mobile Navigation Links -->
        <div class="flex flex-col space-y-6">
          <RouterLink
            to="/"
            class="btn btn-primary text-left"
            @click="closeMobileMenu"
          >
            Home
          </RouterLink>
          <RouterLink
            to="/services"
            class="btn btn-primary text-left"
            @click="closeMobileMenu"
          >
            Services
          </RouterLink>
          <RouterLink
            to="/blogs"
            class="btn btn-primary text-left"
            @click="closeMobileMenu"
          >
            Blogs
          </RouterLink>
          <RouterLink
            to="/about"
            class="btn btn-primary text-left"
            @click="closeMobileMenu"
          >
            About
          </RouterLink>
          <RouterLink
            to="/contact"
            class="btn btn-primary text-left"
            @click="closeMobileMenu"
          >
            Contact
          </RouterLink>
        </div>

        <!-- Mobile User & Book Button -->
        <div class="mt-8 pt-6 border-t border-deep-blue/20">
          <div class="flex items-center space-x-3 mb-4">
            <div
              class="h-8 w-8 flex items-center justify-center rounded-full bg-primary text-white"
            >
              <i class="fa fa-user-circle" />
            </div>
            <span class="text-deep-blue">Profile</span>
          </div>
          <RouterLink
            to="/booking"
            class="btn btn-primary w-full px-4 py-3 bg-bright-blue rounded-lg font-semibold text-white text-center block"
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
const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

// Close mobile menu when route changes
watch(() => useRoute().path, () => {
  closeMobileMenu()
})
</script>
