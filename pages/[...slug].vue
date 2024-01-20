<template>
    <div class="h-full py-2">
        <ContentDoc>
            <template v-slot="{doc}">
                <article class="prose prose-sm max-w-5xl prose-a:text-lavender prose-strong:text-lavender  prose-headings:text-lavender text-mauve lg:prose-xl">        
                    <ContentRenderer :value="doc" />
                </article>
            </template>            
            <template #not-found>
                <NotFound />
            </template>
            <template #empty>
                <NotFound />
            </template>            
        </ContentDoc>
    </div>
</template>    