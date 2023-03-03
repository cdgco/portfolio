<script setup>
defineProps({
  msg: String,
  link: String,
  linkTitle: String
})
</script>

<template>
  <div class="xl:w-4/6 w-5/6">
    <div class="h-screen flex items-center sm:w-4/6 w-5/6">
      <h1 class="text-white font-bold lg:text-8xl md:text-6xl text-5xl relative -top-20">{{ msg }}</h1>
    </div>
    <div class="absolute flex flex-wrap sm:w-4/6 w-5/6 text-white font-bold md:bottom-10 bottom-20">
    <a href="#projects" class="p-4">
      <p> projects <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
          xmlns="http://www.w3.org/2000/svg" class="stroke-2 inline-block h-5 w-5">
          <g>
            <polyline points="6 9 12 15 18 9"></polyline>
          </g>
        </svg></p>
    </a>
    <a :href="link" target="_blank" id="blogLink" class="p-4"
        >
        <p> {{ linkTitle }} 
        <svg width="24" height="24" viewBox="0 0 24 24" stroke="currentColor" stroke-linejoin="round"
            stroke-linecap="round" fill="none" role="presentation" class="stroke-2 inline-block h-5 w-5">
            <line x1="7" y1="17" x2="17" y2="7"></line>
            <polyline points="7 7 17 7 17 17"></polyline>
        </svg></p>
    </a>
  </div>
  </div>
</template>