<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

</script>

<template>
  <nav id="nav" class="bg-gray-800 fixed w-screen z-50">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex-shrink-0 flex items-center">
            <img class="block h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-logo-indigo-500-mark-white-text.svg" alt="Workflow">
          </div>
        </div>
      </div>
    </div>
  </nav>
  <div class="flex bg-gray-800 h-screen">
    <div class="m-auto">
      <h1 class="text-white font-bold xl:text-9xl lg:text-8xl md:text-6xl text-5xl">{{msg}}</h1>
    </div>
  </div>
</template>

<style scoped>
</style>
