<template>
    <header>
        <div>
            <h1>Seção de Comentarios</h1>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    header {
        padding-top: 50px;

        display: flex;
        justify-content: center;
    }

    div {
        padding: 30px 150px;

        border-radius: 30px;
        box-shadow: 0px 5px 5px 1px rgba(0, 0, 0, 0.195);
        background-color: #F22613;
    }

    h1 {
        text-transform: uppercase;
        letter-spacing: 1.2px;
        color: black;
    }
</style>
