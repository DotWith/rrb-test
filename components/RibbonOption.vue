<script setup>
const props = defineProps({
    label: String,
    imgSrc: String,
});
</script>

<template>
    <div>
        <!-- <input type="checkbox" :id="id" :value="value" :checked="isChecked"> -->
        <img :src="imgSrc">
        <label>{{ label }}</label>
        <!-- <input type="range" min="0" max="25" value="0" v-model="devices" @click.stop /> -->
    </div>
</template>
