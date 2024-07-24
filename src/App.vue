<script setup>
import MercuryHeader from './components/MercuryHeader.vue';
</script>

<template>
    <MercuryHeader/>
    <RouterView class="router"/>
</template>

<style scoped>
.router {
    width: 100vw;
}
</style>
