<template>
    <main>
       <CommentContainer />

       <CommentSubmissionContainer />
    </main>
</template>

<script>
    import CommentContainer from "./CommentContainer.vue"
    import CommentSubmissionContainer from "./CommentSubmissionContainer.vue"

    export default {
        name: "MainSection",
        components: {
            CommentContainer, CommentSubmissionContainer
        }
    }
</script>
