<script setup>
import { ref } from 'vue'

defineProps({
    dados: Object
})

const emit = defineEmits(['voltar'])
const mostrarResultado = ref(false)
function voltar() {
    mostrarResultado.value = false
    emit('voltar')
}
</script>

<template>
    <div class="resposta">
        <div class="h1">
            <h1>Informações do usuário</h1>
        </div>
        <div class="pdiv">

            <div class="p">
                <p>Nome: <span> {{ dados.name }}</span></p>
            </div>
            <div class="p">
                <p>Email: <span> {{ dados.email }}</span></p>
            </div>
            <div class="p">
                <p>Senha: <span>{{ dados.senha }}</span></p>
            </div>
            <div class="p">
                <p>Confirmação de senha: <span> {{ dados.senhaConfirma }} </span></p>
            </div>
            <div class="p">
                <p>Nascimento: <span> {{ dados.nascimento }} </span></p>
            </div>
            <div class="p">
                <p>Endereço: <span> {{ dados.endereco }}</span></p>
            </div>
            <div class="p">
                <p>Cidade: <span> {{ dados.cidade }} </span></p>
            </div>
            <div class="p">
                <p>Estado: <span> {{ dados.estado }} </span></p>
            </div>
            <div class="p">
                <p>Hobbies: <span> {{ dados.hobbies }} </span></p>
            </div>
            <div class="p">
                <p>Linguagens: <span> {{ dados.linguagens }} </span></p>
            </div>
            <div class="p" id="rbio">
                <p>Biografia: <span> {{ dados.biografia }} </span></p>
            </div>
        </div>
        <div class="botao">
            <input id="voltar" value="Voltar" @click="voltar()">
        </div>
    </div>
</template>

<style scoped>
.resposta {
    display: flex;
    flex-direction: column;
    margin-top: 50px;
    width: 200%;
    background-color: #38005e83;
    box-shadow: 2px 5px 25px 25px rgba(0, 0, 0, 0.281);
    border-radius: 25px;
    margin-bottom: 10%;
    color: white;
    text-align: center;
    justify-content: center;
    margin-left: 0%;
}

#rbio {
    height: 10vh;
    overflow-y: scroll;
    margin-bottom: 20px;
    margin-top: 20px;
    padding: 10px;
    border-radius: 10px;
    width: 70%;
    margin-left: 15%;
    background-color: white;
    color: black;
    font-size: 15px;
    text-indent: 10px;
    text-align: justify;

}

.resposta input {
    background-color: #440e75;
    color: white;
    height: 5vh;
    margin-left: 0
}

.resposta .pdiv {
    width: 100%;
}

.resposta .p {
    background-color: white;
    color: black;
    width: 70%;
    margin-bottom: 20px;
    height: 5vh;
    margin-left: 15%;
    border-radius: 10px;
    text-align: justify;
    text-indent: 15px;
}

.resposta h1 {
    font-weight: bold;
    margin-bottom: 2.5%;
    margin-top: 2%;
}

span {
    font-weight: bold;
}

.botao {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-bottom: 3%;
    margin-top: 3%;
}

#voltar {
    width: 30%;
    height: 5vh;
    font-size: 20px;
    border-radius: 20px;
    border: 1px solid #000;
    background-color: #440e75;
    color: #fff;
    cursor: pointer;
    margin-right: 5%;
    text-align: center;
}
</style>