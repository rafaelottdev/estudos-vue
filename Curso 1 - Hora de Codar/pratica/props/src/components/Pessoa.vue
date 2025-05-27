<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ name }}</h2>
        <Info :compEmail="email" :esta_trabalhando="esta_trabalhando" />
        <Header :esta_logado=true />
    </div>
</template>

<script>
    import Info from "./Info.vue"
    import Form from "./Form/Form.vue"
    import Header from "./Header.vue"

    export default {
        name: "Pessoa",
        data() {
            return {
                name: "rafael",
                email: "rafa44@gmail.com",
                esta_trabalhando: true
            }
        },
        components: {Info,Form,Header}
    }
</script>
