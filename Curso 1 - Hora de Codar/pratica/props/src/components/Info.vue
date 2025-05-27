<template>
    <div>
        <p>{{ compEmail }}</p>
        <p v-show="esta_trabalhando">Estou trabalhando no momento</p>
    </div>
</template>

<script>
    import Picture from "./Picture.vue"

    export default {
        name: "Info",
        components: {Picture} ,
        props: {
            compEmail: String,
            esta_trabalhando: Boolean
        }
    }
</script>
