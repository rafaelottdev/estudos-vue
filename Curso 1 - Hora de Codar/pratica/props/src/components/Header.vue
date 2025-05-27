<template>
    <ul>
        <li>
            <a href="#">Home</a>
        </li>

        <li>
            <a href="#">Projetos</a>
        </li>

        <li>
            <a href="#">Contato</a>
        </li>

        <li v-if="esta_logado">Meu perfil</li>
    </ul>
</template>

<script>
    export default {
        name: 'Header',
        props: ["esta_logado"]
    }
</script>
