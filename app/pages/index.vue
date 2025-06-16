<script setup lang="ts">
useHead({
  title: 'Nuxt Shadcn',
  meta: [
    { name: 'description', content: 'A minimal Nuxt + shadcn-vue starter application' }
  ]
});

const count = ref(0);
</script>

<template>
    <div class="h-screen flex items-center justify-center">
  <div class="max-w-xl mx-auto p-6 text-center">
    <h1 class="text-3xl font-bold mb-4">Welcome to Nuxt Shadcn!</h1>
    <p class="mb-4">
        This is a minimal Nuxt and shadcn-vue starter application.
    </p>
    <Button
      @click="count++"
    >
      Click me! Count: {{ count }}
    </Button>
  </div>
  </div>
</template>