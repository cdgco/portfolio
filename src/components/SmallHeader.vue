<script setup>
defineProps({
  msg: String
})
</script>

<template>
  <div class="snap-start scroll-m-16 xl:w-4/6 w-5/6">
    <div class="flex md:h-32 h-24 items-center justify-items-start">
      <h1 class="text-white font-bold xl:text-4xl text-3xl">{{ msg }}</h1>
    </div>
  </div>
</template>
