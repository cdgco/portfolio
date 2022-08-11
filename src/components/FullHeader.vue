<script setup>
defineProps({
  msg: String
})
</script>

<template>
  <div class="xl:w-4/6 w-5/6">
    <div class="h-screen flex items-center sm:w-4/6 w-5/6">
      <h1 class="text-white font-bold lg:text-8xl md:text-6xl text-5xl relative -top-20">{{ msg }}</h1>
    </div>
    <a href="#projects" class="absolute sm:w-4/6 w-5/6 text-white font-bold md:bottom-10 bottom-20">
      <p><svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
          xmlns="http://www.w3.org/2000/svg" class="stroke-2 inline-block h-5 w-5">
          <g>
            <polyline points="6 9 12 15 18 9"></polyline>
          </g>
        </svg> projects </p>
    </a>
  </div>
</template>