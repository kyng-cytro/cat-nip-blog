<template>
    <div class="h-full py-2">
        <ContentDoc>
            <template v-slot="{doc}">
                <article class="prose prose-a:text-sapphire prose-strong:text-sapphire  prose-headings:text-sapphire text-pink lg:prose-xl">        
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