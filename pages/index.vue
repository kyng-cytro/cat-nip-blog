<script lang="ts" setup>
const { data } = await useAsyncData('featured', () => queryContent("featured").find())
</script>

<template>
  <div class="max-w-5xl space-y-3 mx-auto">    
    <p class="font-semibold">Featured Post</p>    
    <BlogFeatured :link="data[0]._path" :image="data[0].image" :title="data[0].title" :description="data[0].description" />
    <p class="font-semibold">Recent Post</p>
    <ContentList  v-slot="{ list }">
      <div class="flex flex-wrap gap-3">
      <BlogCard :link="article._path" :title="article.title" :description="article.description" v-for="article in list" :key="article._path"/>      
    </div>
    </ContentList>
  </div>
</template>
