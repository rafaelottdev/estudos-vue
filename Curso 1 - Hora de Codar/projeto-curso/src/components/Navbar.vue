<template>
    <nav id="nav">
        <RouterLink to="/" id="logo_url">
            <img :src="logo" :alt="alt" id="logo">
        </RouterLink>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/pedidos">Pedidos</RouterLink>
    </nav>
</template>

<script>
    export default {
        name: "Navbar",
        props: ["logo", "alt"]
    }
</script>

<style scoped>
    #nav {
        padding: 15px 50px;

        display: flex;
        align-items: center;
        justify-content: flex-end;

        border-bottom: 4px solid #111;
        background-color: #222;
    }

    #nav #logo_url {
        margin: auto;
        margin-left: 0;
    }

    #logo {
        width: 40px;
        height: 40px;
    }

    #nav a {
        margin: 12px;

        text-decoration: none;
        color: #fcba03;
        transition: .5s;
    }

    #nav a:hover {
        color: #FFF;
    }
</style>