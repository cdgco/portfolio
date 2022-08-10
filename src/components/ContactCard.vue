<script setup>
defineProps({
  title: String,
  subtitle: String,
  link: String,
  icon: String,
})
</script>

<template>
  <a :href="link" target="_blank"
    class="containter my-2.5 mx-0 lg:mr-2.5 lg:w-2/6 w-full p-10 border-b bg-white hover:bg-slate-200 cursor-pointer rounded-xl font-sans text-left">
    <h2 :class="'text-' + color + '-400'" class="font-normal pb-2 text-2xl"><i class="fa" :class="'fa-' + icon"
        aria-hidden="true"></i> {{ title }}</h2>
    <p :class="'text-' + color + '-400'" class="font-normal pb-2 text-md">{{ subtitle }}</p>
  </a>
</template>