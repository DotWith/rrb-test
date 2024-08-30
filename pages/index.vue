<script setup>
const { data } = await useAsyncData('ribbons', () => queryContent('/ribbons_meta').findOne());

function getRibbonSvgPath(id) {
  return `/ribbons/${id}.svg`;
}
</script>

<template>
    <div>
        <h1>Welcome to the homepage</h1>
        <ContentDoc />
        <div v-for="ribbon in data.body" :key="ribbon.id">
            <RibbonOption :label="`${ribbon.id}. ${ribbon.name}`" :imgSrc="getRibbonSvgPath(ribbon.id)" />
            <!-- <img :src="`/ribbons/${ribbon.id}.svg`" /> -->
        </div>
        <AppAlert>
            This is an auto-imported component
        </AppAlert>
    </div>
</template>
