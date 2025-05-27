<template>
    <div>
        <Header />
        <Info />
        <p class="paragrafo-pai">O dado de app é testando</p>
    </div>
</template>

<script>
    import Info from "./components/Info.vue"
    import Header from "./components/Header.vue"

    export default {
        name: 'App', components: {Info, Header}
    }
</script>

<style>
    body {
        background-color: black;
        color: white;
    }

    a {
        color: red;
    }

    .teste {
        background-color: black;
    }
</style>