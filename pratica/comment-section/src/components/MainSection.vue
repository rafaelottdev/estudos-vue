<template>
    <main>
       <CommentContainer :commentList="commentList" />

       <CommentSubmissionContainer :getNameValue="getNameValue" :getCommentValue="getCommentValue" :sendComment="sendComment" />
    </main>
</template>

<script>
    import CommentContainer from "./CommentContainer.vue"
    import CommentSubmissionContainer from "./CommentSubmissionContainer.vue"

    export default {
        name: "MainSection",
        data() {
            return {
                currentNameValue: '',
                currentCommentValue: '',
                nameInputElement: '',
                commentInputElement: '',
                commentList: []
            }
        },
        components: {
            CommentContainer, CommentSubmissionContainer
        },
        methods: {
            getNameValue(e) {
                this.currentNameValue = e.target.value
                this.nameInputElement = e.target
            },
            getCommentValue(e) {
                this.currentCommentValue = e.target.value
                this.commentInputElement = e.target
            },
            sendComment() {
                this.nameInputElement.value = ''
                this.nameInputElement.focus()
                this.commentInputElement.value = ''

                if(this.commentList.length >= 0) {
                    this.commentList = [...this.commentList, {name: this.currentNameValue, comment: this.currentCommentValue}]
                }
            }
        }
    }
</script>
