<template>
    <div>
        <Pessoa />
    </div>
</template>

<script>
    import Form from "./components/Form/Form.vue"
    import PrimeiroComponente from "./components/PrimeiroComponente.vue"
    import Pessoa from "./components/Pessoa.vue"

    export default {
        name: 'App', components: {Form, PrimeiroComponente, Pessoa}
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
