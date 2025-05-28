<template>
    <section>
        <div>
            <input type="text">
            <textarea></textarea>
            <button>Comentar</button>
        </div>
    </section>
</template>

<script>
    export default {
        name: "CommentSubmissionContainer"
    }
</script>

<style scoped>
    section {
        padding-top: 50px;

        display: flex;
        justify-content: center;
    }

    div {
        display: flex;
        flex-direction: column;
    }

    div > input {
        height: 35px;
        margin-bottom: 10px;

        font-size: 1.1em;
        letter-spacing: 1px;
    }

    div > textarea {
        height: 130px;
        margin-bottom: 20px;

        font-size: 1.1em;
        line-height: 1.5em;
        letter-spacing: .8px;

        resize: none;
    }

    div > button {
        height: 50px;

        font-size: 1.2em;
        font-weight: bold;
        text-transform: uppercase;
        letter-spacing: 1px;

        border-radius: 5px;
        color: white;
        background-color: #02554d;
    }

    div > button:hover {
        cursor: pointer;
        background-color: #013b35;
    }

    input, textarea {
        width: 480px;
        padding: 10px;

        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        border-radius: 5px;
        color: white;
        background-color: #02554d;
    }
</style>
