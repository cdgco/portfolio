<script setup>
defineProps({
    title: String,
    subtitle: String,
    description: String,
    date: String,
    textColor: String,
    buttonColor: String,
    buttonHover: String,
    link: String,
    icons: Array
})
</script>

<template>
    <div id="smallCard"
        class="containter my-2.5 mx-0 lg:w-3/6 w-full p-12 border-b bg-white rounded-xl font-sans text-left snap-start scroll-m-16">
        <h2 :class="textColor" class="font-normal pb-2 md:text-2xl sm:text-xl text-lg">{{ subtitle }}</h2>
        <span class="inline-flex items-baseline">
            <h1 class="font-extrabold md:text-3xl sm:text-2xl text-xl">{{ title }}</h1>
            <h2 class="pl-2 font-bold text-gray-500 md:text-md sm:text-sm text-xs">{{ date }}</h2>
        </span>
        <div class="grid grid-cols-3 gap-8 pt-10">
            <div class="col-span-3 text-gray-600 relative">
                <p class="">{{ description }}</p>
                <br class="lg:block hidden">
            </div>
            <div class="lg:col-span-3 sm:col-span-2 col-span-3 relative">
                <div class="bottom-0 left-0 text-sm font-medium p-2 inline-flex items-center">
                    <p class="h-full pr-4 sm:block hidden">BUILT WITH</p>
                    <span v-for="(icon, index) in icons" v-bind:key="index" class="pr-2">
                        <img class="rounded-lg shadow p-1 h-10 w-10" :src="icon">
                    </span>
                </div>
            </div>
            <div class="lg:col-span-3 sm:col-span-1 col-span-3 relative inline-grid items-center">
                <a :href="link" target="_blank">
                    <button type="button" :class="buttonColor + ' hover:' + buttonHover"
                        class="shadow w-full rounded-lg text-white font-medium transition-colors duration-150 cursor-pointer inline-flex items-center justify-center flex-row px-5 py-2">
                        View Project
                        <span class="w-4 h-4 inline-flex items-center ml-1">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-linecap="round"
                                stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg"
                                class="stroke-2 inline-block h-4 w-4">
                                <g>
                                    <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                                    <polyline points="15 3 21 3 21 9"></polyline>
                                    <line x1="10" y1="14" x2="21" y2="3"></line>
                                </g>
                            </svg>
                        </span>
                    </button>
                </a>
            </div>
        </div>
    </div>
</template>