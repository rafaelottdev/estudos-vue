<template>
    <div>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="tech in backend_tech">{{ tech }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end</p>
        <ul>
            <li v-for="tech in front_tech" :key="tech.id">{{ tech.language }}</li>
        </ul>
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
                meu_link: 'https://google.com',
                backend_tech: ['javascript', "PHP", "Python"],
                front_tech: [
                    {id: 1, language: "HTML"},
                    {id: 2, language: "CSS"},
                    {id: 3, language: "Vue"}
                ]
            }
        }
    }
</script>

<style>
    .paragrafo-pai {
        color: red;
    }
</style>
