<script lang="ts" setup>
defineProps({
    link: String,
    image: String,
    title: String,
    description: String,
})
</script>

<template>
    <NuxtLink :to="link" class="flex flex-col bg-lavender items-center rounded-lg shadow md:flex-row">
        <img class="object-cover w-full rounded-t-lg h-48 md:h-auto md:w-48 md:rounded-none md:rounded-s-lg" :src="image" :alt="title">
        <div class="flex flex-col justify-between p-4 leading-normal">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-crust">{{ title }}</h5>
            <p class="mb-3 font-normal text-surface2 line-clamp-3">{{ description }}</p>
        </div>
    </NuxtLink>
</template>