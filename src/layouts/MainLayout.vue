<script setup>
    import Footer from '@/components/Footer.vue';
    import Header from '@/components/Header.vue';
    import Home from '@/views/Home.vue';
</script>
<template>
    <Header></Header>
    <router-view></router-view>
    <About></About>
</template>