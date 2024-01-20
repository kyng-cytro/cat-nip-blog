<script lang="ts" setup>
defineProps({
    link:String,
    title: String,
    description: String    
})
</script>

<template>
    <div class="md:max-w-sm p-4 bg-lavender border border-blue rounded-lg shadow">
    <NuxtLink :to="link">
        <h5 class="text-crust mb-2 text-2xl font-semibold tracking-tight line-clamp-1">{{ title }}</h5>
    </NuxtLink>
    <p class="mb-3  text-surface2 font-normal line-clamp-3">{{ description }}</p>
    <NuxtLink :to="link" class="inline-flex items-center px-2 py-1.5 text-sm font-medium text-center rounded-lg text-red hover:text-mauve">
        Read more
        <Icon name="uil:arrow-right" height="25" width="25"/>
    </NuxtLink>
</div>
</template>