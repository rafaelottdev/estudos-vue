<template>
    <div class="message-container">
        <p>{{ msg }}</p>
    </div>
</template>

<script>
    export default { 
        name: "Message",
        props: {
            msg: String
        }
    }
</script>

<style scoped>
    .message-container {
        max-width: 400px;

        margin: 30px auto;
        padding: 10px;

        border: 2px solid #b8daff;
        border-radius: 5px;
        color: #004085;
        background-color: #cce5ff;
    }
</style>
