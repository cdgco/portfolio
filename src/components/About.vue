<script setup>
defineProps({
  msg: String
})
</script>

<template>
  <div class="mx-5 snap-start scroll-m-16 my-2.5 w-full flex content-start">
    <div class="containter m-auto xl:w-4/6 w-5/6 font-sans text-left">
      <div style="font-size: 16px; letter-spacing: 5px;left: 10px;position: relative;line-height: 0px;top: 25px;">
        <span class="text-red-500 cursor-pointer">●</span><span class="text-yellow-400 cursor-pointer">●</span><span
          class="text-green-500 cursor-pointer">●</span>
      </div>
      <pre style="border-width:0px !important;" class="language-php rounded-xl">
        <code class="language-php">

        {{ msg }}

        </code>
      </pre>
    </div>
  </div>
</template>
