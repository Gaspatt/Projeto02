<script setup>
import { reactive, ref} from 'vue'



const dados = reactive({
  name: '',
  email: '',
  senha: '',
  senhaConfirma: '',
  nascimento: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: '',
  linguagens: '',
  biografia: ''
})


const emit = defineEmits(['enviar'])

const mostrarResultado = ref(false)

function enviar() {
    emit('enviar', dados)
    mostrarResultado.value = true
}



</script>

<template>
  <form @submit.prevent="enviar">
    <div class="divmain">
      <div class="div">
        <label for="name">Nome:</label>
        <input type="text" id="name" v-model="dados.name" />

        <label for="email">Email:</label>
        <input type="email" id="email" v-model="dados.email" />

        <label for="senha">Senha:</label>
        <input type="password" id="senha" v-model="dados.senha" />

        <label for="senhaConfirma">Confirme a senha:</label>
        <input type="password" id="senhaConfirma" v-model="dados.senhaConfirma" />

        <label for="nascimento">Data de Nascimento:</label>
        <input type="date" id="nascimento" v-model="dados.nascimento" />

        <label for="endereco">Endereço:</label>
        <input type="text" id="endereco" v-model="dados.endereco" />

        <label for="cidade">Cidade:</label>
        <input type="text" id="cidade" v-model="dados.cidade" />

        <label for="estado">Estado:</label>
        <select id="estado" name="estado" v-model="dados.estado">
          <option value="Acre">Acre</option>
          <option value="Alagoas">Alagoas</option>
          <option value="Amapá">Amapá</option>
          <option value="Amazonas">Amazonas</option>
          <option value="Bahia">Bahia</option>
          <option value="Ceará">Ceará</option>
          <option value="Distrito Federal">Distrito Federal</option>
          <option value="Espírito Santo">Espírito Santo</option>
          <option value="Goiás">Goiás</option>
          <option value="Maranhão">Maranhão</option>
          <option value="Mato Grosso">Mato Grosso</option>
          <option value="Mato Grosso do Sul">Mato Grosso do Sul</option>
          <option value="Minas Gerais">Minas Gerais</option>
          <option value="Pará">Pará</option>
          <option value="Paraíba">Paraíba</option>
          <option value="Paraná">Paraná</option>
          <option value="Pernambuco">Pernambuco</option>
          <option value="Piauí">Piauí</option>
          <option value="Rio de Janeiro">Rio de Janeiro</option>
          <option value="Rio Grande do Norte">Rio Grande do Norte</option>
          <option value="Rio Grande do Sul">Rio Grande do Sul</option>
          <option value="Rondônia">Rondônia</option>
          <option value="Roraima">Roraima</option>
          <option value="Santa Catarina">Santa Catarina</option>
          <option value="São Paulo">São Paulo</option>
          <option value="Sergipe">Sergipe</option>
          <option value="Tocantins">Tocantins</option>
        </select>

        <label for="hobbies">Hobbies:</label>
        <input type="text" id="hobbies" v-model="dados.hobbies" />

        <label for="linguagens">Linguagens de Programação:</label>
        <input type="text" id="linguagens" v-model="dados.linguagens" />

        <label for="biografia">Biografia:</label>
        <textarea id="biografia" v-model="dados.biografia"></textarea>
      </div>
    </div>
    <button type="submit" @click="enviar()">Enviar</button>
  </form>
</template>

<style scoped>

body {
    background-color: white;
}

span {
    font-weight: bold;
}

.checkbox {
    color: rgb(255, 255, 255);
    width: 50%;
    margin-left: 15%;
    display: flex;
    align-items: end;
}

.checkbox label {
    color: rgb(255, 255, 255);
    margin-left: 10px;

}

.radio {
    color: rgb(255, 255, 255);
    width: 50%;
    margin-left: 12%;
    display: flex;
    align-items: end;
}

.radio label {
    color: rgb(255, 255, 255);
    margin-left: 10px;
}

.h1 {
    width: 100%;
    text-align: center;
    font-size: 1.5rem;
    color: rgb(0, 0, 0);
    font-weight: bolder;
    margin-top: 1vh;
    margin-bottom: 1vh;
}

h1 {
    font-weight: bold;

}

.form {
    display: flex;
    flex-direction: column;
    box-shadow: 2px 5px 25px 25px rgba(0, 0, 0, 0.281);
    margin-top: 50px;
    width: 200%;
    background-color: #38005e83;
    border-radius: 25px;
    margin-bottom: 10%;

}

.checkbox input {
    margin-left: 8%;
}

.divv {
    border-radius: 25px;
}

.poppins-light {
    font-family: "Poppins", sans-serif;
    font-weight: 300;
    font-style: normal;
}

input {
    width: 70%;
    padding: 5px;
    height: 30px;
    margin-left: 15%;
    margin-bottom: 4vh;
    border-radius: 15px;
    border: 1px solid #000;
    margin-top: 2px;
    margin-bottom: 10px;
    font-family: "Poppins", sans-serif;
    font-weight: 5 00;
    font-style: normal;
    font-size: 15px;

}

label {
    margin-left: 15%;
    margin-top: 10px;
    color: #fff;
    margin-bottom: 1vh;
    font-size: 18px;
}



.ast {
    color: red;
}

select {
    width: 70%;
    height: 30px;
    margin-left: 15%;
    border-radius: 5px;
    border: 1px solid #000;
}

.botoes {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-bottom: 3%;
    margin-top: 3%;
}
button[type="submit"] {
    width: 30%;
    height: 5vh;
    font-size: 20px;
    border-radius: 20px;
    border: 1px solid #000;
    background-color: #440e75;
    color: #fff;
    cursor: pointer;
    margin-right: 5%
}

button[type="reset"] {
    width: 30%;
    height: 5vh;
    font-size: 20px;
    border-radius: 20px;
    border: 1px solid #000;
    background-color: #5c5275;
    color: #fff;
    cursor: pointer;
}

select {
    border-radius: 15px;
    padding: 5px;
}

option {
    cursor: pointer;
}

textarea {
    resize: none;
    border-radius: 15px;
    width: 70%;
    margin-left: 15%
}

</style>
