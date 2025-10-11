<template>
  <div class="pb-10">
    <nav
      class="flex items-center justify-between px-10 py-1 bg-soft-blue text-deep-blue font-size-16 font-medium text-center rounded-2xl"
    >
      <RouterLink to="/">
        <img
          src="../assets/images/logo.svg"
          class="w-24 h-24"
          alt="todo list logo"
        />
      </RouterLink>
      <div class="flex items-center space-x-8">
        <RouterLink to="/create" class="btn btn-primary">Home</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Services</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Blogs</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">About</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Contact</RouterLink>
      </div>
      <div class="flex items-center justify-items-center space-x-5">
        <div
          class="h-8 w-8 flex items-center justify-center rounded-full bg-primary text-white"
        >
          <i class="fa fa-user-circle"></i>
        </div>
        <RouterLink
          to="/booking"
          class="btn btn-primary px-7 py-3.5 bg-bright-blue rounded-lg font-semibold text-white"
          >Book Now</RouterLink
        >
      </div>
    </nav>
  </div>
</template>
<script setup lang="ts"></script>
