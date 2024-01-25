<script lang="ts" setup>
defineProps({
    link:String,
    title: String,
    description: String    
})
</script>

<template>
    <div class="md:max-w-sm p-4 bg-lavender border border-blue rounded-lg shadow">
    <NuxtLink class="hover:animate-pulse underline" :to="link">
        <h5 class="text-crust mb-2 text-2xl font-semibold tracking-tight line-clamp-1">{{ title }}</h5>
    </NuxtLink>
    <p class="mb-3  text-surface2 font-normal line-clamp-4">{{ description }}</p>
</div>
</template>