<template>
    <main>
        <section class="panel-section">
            <div class="panel-list-container">
                <ul class="panel-list">
                    <li>Mais Vendidos</li>
                    <li>Novidades</li>
                    <li>Carrinho</li>
                    <li>Favoritos</li>
                </ul>
            </div>

            <div class="content-container"></div>
        </section>
    </main>
</template>

<script>
    export default {
        name: "MainSection"
    }
</script>

<style scoped>
    .panel-section {
        width: 100%;
        height: calc(100vh - 80px);

        background-color: red;
    }

    .panel-list-container {
        width: 1000px;
        margin: 0 auto;
        padding-top: 50px;

        display: flex;
    }

    .panel-list {
        width: inherit;
        display: flex;
        justify-content: space-between;
    }

    .panel-list > li {
        padding: 8px 30px;

        border-top-left-radius: 5px;
        border-top-right-radius: 5px;

        font-weight: bold;
        font-size: .9em;
        letter-spacing: 1px;
        text-transform: uppercase;
        font-family: sans-serif;

        cursor: pointer;

        color: white;
        background-color: rgb(95, 23, 23);
    }

    .content-container {
        width: 1000px;
        height: 80%;

        margin: 0 auto;

        background-color: rgb(95, 23, 23);
    }
    
</style>
