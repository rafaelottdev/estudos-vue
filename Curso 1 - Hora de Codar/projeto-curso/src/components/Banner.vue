<template>
    <div id="main-banner">
        <h1>Make Your Burguer</h1>
    </div>
</template>

<script>
    export default {
        name: "Banner"
    }
</script>

<style scoped>
    #main-banner{
        height: 600px;

        display: flex;
        align-items: center;
        justify-content: flex-start;

        background-image: url('/public/img/burger.jpg');
        background-position: 0 -250px;
        background-size: cover;
        background-repeat: no-repeat;
    }

    #main-banner h1 {
        padding: 20px 40px;

        text-align: center;
        font-size: 60px;

        color: #fff;
        background-color: #222;
    }
</style>
