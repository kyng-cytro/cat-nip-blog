<template>
    <div class="h-full">
        <ContentDoc>
            <template v-slot="{doc}">
                <article class="prose lg:prose-xl">
                    <h1>{{ doc.title }}</h1>
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