<template>
  <header>
    <TheNavigation />
  </header>
  <!-- <main class="mx-auto pt-6 sm:w-full sm:px-4 lg:w-4/6 lg:px-0"> -->
  <main class="fixed top-16 bottom-0 w-full overflow-y-scroll">
    <div class="mx-auto w-3/4 pt-4">
      <RouterView />
    </div>
  </main>
</template>

<script setup lang="ts">
import TheNavigation from '@/components/TheNavigation.vue';
</script>
