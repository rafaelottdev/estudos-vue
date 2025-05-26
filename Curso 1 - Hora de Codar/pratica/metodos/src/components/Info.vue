<template>
    <div>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
            <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Info",
        data() {
            return {
                mostrar_email: false,
                email: 'rafaelott333@gmail.com',
                textoBotao: "Mostrar Email"
            }
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email) {
                    this.textoBotao = "Mostrar Email"
                }

                else {
                    this.textoBotao = "Esconder Email"
                }
            }
        }
    }
</script>
