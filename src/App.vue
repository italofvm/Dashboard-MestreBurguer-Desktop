<script setup>
import { RouterView } from 'vue-router'
import TheSidebar from '@/components/TheSidebar.vue'
import TheHeader from '@/components/TheHeader.vue'
</script>

<template>
  <div class="grid grid-cols-[260px_1fr] h-full">
    <div class="w-[260px]">
      <TheHeader />
      <TheSidebar />
    </div>
    <main class="mx-2 my-20 px-3 py-2 bg-[#f8f8f8] rounded-2xl">
      <RouterView />
    </main>
  </div>
</template>

<style scoped></style>
