<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ name }}</h2>
        <Info />
        <Form />
    </div>
</template>

<script>
    import Info from "./Info.vue"
    import Form from "./Form/Form.vue"

    export default {
        name: "Pessoa",
        data() {
            return {
                name: "rafael"
            }
        },
        components: {
            Info,
            Form
        }
    }
</script>
