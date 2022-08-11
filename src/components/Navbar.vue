<script setup>
defineProps({
    title: String,
    link: String,
    linkTitle: String,
})
</script>

<template>
    <nav id="nav" class="sticky top-0 z-50 opacity-0 snap-start">
        <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
                    <div class="flex-shrink-0 flex items-center">
                        <h2 class="text-white font-bold text-2xl"><a href="/">{{ title }}</a></h2>
                    </div>
                </div>
                <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
                    <a href="{{link}}" target="_blank"
                        class="text-white inline-flex hover:bg-blue-500 hover:text-white px-3 py-2 rounded-md text-sm font-medium">
                        {{ linkTitle }}
                        <svg width="24" height="24" viewBox="0 0 24 24" stroke="currentColor" stroke-linejoin="round"
                            stroke-linecap="round" fill="none" role="presentation" class="stroke-2 w-4 h-4 ml">
                            <line x1="7" y1="17" x2="17" y2="7"></line>
                            <polyline points="7 7 17 7 17 17"></polyline>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </nav>
</template>