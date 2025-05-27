<template>
    <form @submit="enviarForm($event)">
        <input type="text" v-model="name">
         <input type="text" v-model="email">
        <Submit />
    </form>
</template>

<script>
    import InputText from "./InputText.vue"
    import Submit from "./Submit.vue"

    export default {
        name: "Form",
        components: {
            InputText,
            Submit
        },
        data() {
            return {
                name: '',
                email: ''
            }
        },
        methods: {
            enviarForm(e) {
                e.preventDefault()
                const name = this.name
                const email = this.email

                console.log(`o nome é ${name} e o email é ${email}`)
            }
        }
    }
</script>
