<script lang="ts" setup>
  const theme = useCookie("color-scheme", {default: () => "mocha", maxAge: 10 * 365 * 24 * 60 * 60 })
</script>
<template>
  <div 
    class="flex flex-col min-h-screen bg-base font-mono text-mauve"
    :class="theme"
  >
    <Nav  />
    <main class="flex-1 p-2">
      <NuxtPage />
    </main>
    <Footer />
  </div>
</template>
