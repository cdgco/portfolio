<script setup>
defineProps({
  msg: String
})
</script>

<template>
  <div class="flex items-center justify-center bg-gray-200 w-full">
    <div class="h-16 p-5 xl:w-4/6 w-5/6">
      <h1>&copy; {{ new Date().getFullYear() }} {{ msg }}. All Right Reserved.</h1>
    </div>
  </div>
</template>