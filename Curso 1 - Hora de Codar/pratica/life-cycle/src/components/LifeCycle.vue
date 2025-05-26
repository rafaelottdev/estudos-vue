<template>
    <h1>Meu nome é: {{ name }}</h1>
</template>

<script>
    export default {
        name: "LifeCycle",
        data() {
            return {
                name: "ainda não sei"
            }
        },
        created() {
            this.name = "matheus"
        },
        mounted() {
            this.name = "pedro"
        }
    }
</script>
