<script setup>
defineProps({
    title: String,
    subtitle: String,
})
</script>

<template>
    <div class="snap-start mx-5 my-2.5 mb-20 snap-start scroll-m-16 xl:w-4/6 w-5/6">
        <div class="flex content-start lg:flex-row flex-col">
            <slot></slot>
        </div>
    </div>
</template>