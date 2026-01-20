<script setup>
import { ref } from 'vue'
const open = ref(false)
</script>

<template>
  <header class="flex items-center justify-between p-4 border-b">
    <div class="font-bold text-xl">Logo</div>

    <button class="md:hidden" @click="open = !open">
      ☰
    </button>

    <nav
      :class="open ? 'block' : 'hidden'"
      class="absolute top-16 left-0 w-full bg-white md:static md:block"
    >
      <ul class="flex flex-col md:flex-row gap-4 p-4">
        <li>Home</li>
        <li>Features</li>
        <li>Contact</li>
      </ul>
    </nav>
  </header>
</template>
