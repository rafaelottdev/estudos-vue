<template>
    <img :src="avatar" :alt="descricao">
    <MudarImg @trocar-img="trocarImg"  />
</template>

<script>
    import MudarImg from "./MudarImg.vue"

    export default {
        name: "Picture",
        components: {MudarImg},
        data() {
            return {
                avatar: "/img/avatar.png",
                descricao: "rafael ott"
            }
        },
        methods: {
            trocarImg() {
                this.avatar = "/img/avatar2.png"
            }
        }
    }
</script>
