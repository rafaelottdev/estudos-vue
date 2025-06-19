<template>
    <div id="burguer-table">
        <Message :msg="msg" v-show="msg" />
        <div>
            <div id="burguer-table-heading">
                <div class="order-id">#:</div>
                <div>Cliente:</div>
                <div>Pão:</div>
                <div>Carne:</div>
                <div>Opcionais:</div>
                <div>Ações:</div>
            </div>
        </div>

        <div id="burguer-table-rows">
            <div class="burguer-table-row" v-for="burguer in burguers" :key="burguer.id">
                <div class="order-number">{{ burguer.id }}</div>
                <div>{{ burguer.nome }}</div>
                <div>{{ burguer.pao }}</div>
                <div>{{ burguer.carne }}</div>

                <div>
                    <ul>
                        <li v-for="(opcional, index) in burguer.opcionais" :key="index">
                            {{ opcional }}
                        </li>
                    </ul>
                </div>

                <div>
                    <select name="status" class="status" @change="updateBurguer($event, burguer.id)">
                        <option v-for="s in status" :key="s.id" :value="s.tipo" :selected="burguer.status == s.tipo">
                            {{ s.tipo }}
                        </option>
                    </select>
                    <button class="delete-btn" @click="deleteBurguer(burguer.id)">Cancelar</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Message from './Message.vue'

    export default {
        name: "Dashboard",
        data() {
            return {
                burguers: null,
                burguer_id: null,
                status: [],
                 msg: null
            }
        },
        components: {Message},
        methods: {
            async getPedidos() {
                const req = await fetch("http://localhost:3000/burguers")
                const data = await req.json()

                this.burguers = data

                this.getStatus()
            },
            async getStatus() {
                const req = await fetch('http://localhost:3000/status')
                const data = await req.json()

                this.status = data
            },
            async deleteBurguer(id) {
                const req = await fetch(`http://localhost:3000/burguers/${id}`, {
                    method: "DELETE"
                })

                const res = await req.json()

                this.msg = `Pedido removido com Sucesso!`

                setTimeout(() => this.msg = "", 1000)

                this.getPedidos()
            },
            async updateBurguer(event, id) {
                const option = event.target.value

                const dataJson = JSON.stringify({ status: option })

                const req = await fetch(`http://localhost:3000/burguers/${id}`, {
                    method: "PATCH",
                    headers: { "Content-Type": "application/json" },
                    body: dataJson
                })

                const res = await req.json()

                this.msg = `O pedido N° ${res.id} foi atualizado para ${res.status}!`

                setTimeout(() => this.msg = "", 1500)
            }
        },
        mounted() {
            this.getPedidos()
        }
    }
</script>

<style scoped>
    #burguer-table {
        max-width: 1200px;
        margin: 0 auto;

    }

    #burguer-table-heading, #burguer-table-rows, .burguer-table-row {
        display: flex;
        flex-wrap: wrap;
    }

    #burguer-table-heading {
        padding: 12px;
        font-weight: bold;
        border-bottom: 3px solid #333;
    }

    #burguer-table-heading > div, .burguer-table-row div {
        width: 19%;
    }

    .burguer-table-row {
        width: 100%;
        padding: 12px;
        border-bottom: 1px solid #ccc;
    }

    #burguer-table-heading .order-id, .burguer-table-row .order-number {
        width: 5%;
    }

    select {
        margin-right: 12px;
        padding: 12px 6px;
    }

    .delete-btn {
        padding: 10px;
        margin: 0 auto;

        font-size: 16px ;
        font-weight: bold;

        cursor: pointer;
        border: 2px solid #222;
        color: #fcba03;
        background-color: #222;

        transition: .5s;
    }

    .delete-btn:hover {
        color: #222;
        background-color: transparent;
    }
</style>
