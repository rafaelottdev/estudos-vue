<template>
    <Navbar />

    <MainSection />
</template>

<script>
    import Navbar from './components/Navbar.vue'
    import MainSection from './components/MainSection.vue';

    export default {
        components: {
            Navbar, MainSection
        }
    }
</script>

<style>
 * {
    margin: 0;
    padding: 0;
    outline: 0;
    box-sizing: border-box;
    list-style: none;
 }
</style>
