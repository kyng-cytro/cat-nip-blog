<script lang="ts" setup>
const themes = ['frappe', "macchiato",'mocha']
const theme = useCookie("color-scheme")
</script>
<template>
    <select id="theme-switcher" name="theme-switcher" v-model="theme" class="tracking-tighter text-sm rounded-lg px-1 focus:outline-none capitalize bg-lavender">
        <option :key="theme" :value="theme" v-for="theme in themes">{{ theme }}</option>
    </select>
</template>