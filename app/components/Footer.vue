<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div class="flex items-center justify-between">
      <RouterLink to="/">
        <img
          src="../assets/images/logo.svg"
          class="w-24 h-24"
          alt="todo list logo"
        />
      </RouterLink>
      <div class="flex items-center text-deep-blue space-x-8">
        <RouterLink to="/create" class="btn btn-primary">Home</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Services</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Blogs</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">About</RouterLink>
        <RouterLink to="/create" class="btn btn-primary">Contact</RouterLink>
      </div>
    </div>
    <hr class="my-4 border-t-4 border-deep-blue" />
    <div class="flex items-center justify-between">
      <p class="text-gray-600 dark:text-gray-400">
        &copy; {{ new Date().getFullYear() }} All rights reserved ® uifry.com |
        Terms and conditions apply!
      </p>
      <div class="flex items-center space-x-4">
        <a href="#">
          <img
            src="../assets/icon/facebook.svg"
            alt="Facebook"
            class="w-8 h-8"
          />
        </a>
        <a href="#">
          <img
            src="../assets/icon/instagram.svg"
            alt="Instagram"
            class="w-8 h-8"
          />
        </a>
        <a href="#">
          <img src="../assets/icon/youtube.svg" alt="YouTube" class="w-8 h-8" />
        </a>
        <a href="#">
          <img
            src="../assets/icon/linkedin.svg"
            alt="LinkedIn"
            class="w-8 h-8"
          />
        </a>
        <a href="#">
          <img src="../assets/icon/twitter.svg" alt="Twitter" class="w-8 h-8" />
        </a>
      </div>
    </div>
  </div>
</template>
