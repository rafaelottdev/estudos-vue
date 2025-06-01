<template>
    <section>
        <div>
            <ul>
                <li v-for="(comment, index) in commentList" :key="index">
                    <p>{{ comment.name }}</p>
                    <p>{{ comment.comment }}</p>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
    export default {
        name: "CommentContainer",
        props: {
            commentList: Array
        }
    }
</script>

<style scoped>
    section {
        padding-top: 20px;

        display: flex;
        align-items: center;
        justify-content: center;
    }

    div {
        width: 1000px;
        min-height: 200px;

        padding: 25px;

        border-radius: 30px;

        overflow-wrap: break-word;

        color: white;
        background-color: #0C1A26;
    }

    li {
        margin-bottom: 20px;
    }

    li > p:first-child {
        margin-bottom: 5px;
        padding: 3px 5px;

        display: inline-block;
        border-radius: 5px;

        font-size: .8em;
        letter-spacing: 1px;

        background-color: rgba(0, 0, 0, 0.364);
    }
</style>
