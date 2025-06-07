<template>
    <div>
        <p>Componente de mensagem</p>

        <div>
            <form id="burguer-form">
                <div class="input-container">
                    <label for="nome">Nome do cliente:</label>
                    <input type="text" id="nome" name="nome" v-model="nome" placeholder="Digite o seu nome">
                </div>

                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu pão</option>
                        <option value="Integral">Integral</option>
                    </select>
                </div>

                <div class="input-container">
                    <label for="carne">Escolha a carne do seu Burguer:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione o tipo de carne</option>
                        <option value="maminha">Maminha</option>
                    </select>
                </div>

                <div id="opcionais-container" class="input-container">
                    <label id="opcionais-title" for="opcionais">Selecione os opcionais:</label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" id="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span>
                    </div>

                     <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" id="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span>
                    </div>

                     <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" id="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span>
                    </div>
                </div>

                <div class="input-container">
                    <input type="submit" class="submit-btn" value="Criar Meu Burguer!">
                </div>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "BurguerForm"
    }
</script>

<style scoped>
    #burguer-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        margin-bottom: 20px;

        display: flex;
        flex-direction: column;
    }

    label {
        margin-bottom: 15px;
        padding: 5px 10px;
        font-weight: bold;

        border-left: 4px solid #fcba03;
        color: #222;
    }

    input, select {
        width: 300px;
        padding: 5px 10px;
    }

    #opcionais-container {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #opcionais-title {
        width: 100%;
    }
    
    .checkbox-container {
        width: 50%;
        margin-bottom: 20px;

        display: flex;
        align-items: flex-start;
    }

    .checkbox-container span, .checkbox-container input {
        width: auto;
    } 

    .checkbox-container span {
        margin-left: 6px;
        font-weight: bold;
    }

    .submit-btn {
        margin: 0 auto;
        padding: 10px;

        font-size: 16px;
        font-weight: bold;

        cursor: pointer;
        border: 2pxs solid #222;
        color: #fcba03;
        background-color: #222;

        transition: .5s;
    }

    .submit-btn:hover {
        color: #222;
        background-color: transparent;
    }
</style>