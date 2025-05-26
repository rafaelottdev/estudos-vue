<template>
    <div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portfolio <a v-bind:href="meu_link">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
    import Picture from "./Picture.vue"

    export default {
        name: "Info",
        components: {Picture} ,
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email: true,
                email: 'rafaelott333@gmail.com',
                meu_link: 'https://google.com'
            }
        }
    }
</script>

<style>
    .paragrafo-pai {
        color: red;
    }
</style>
