<script setup>
import { reactive } from 'vue'

const props = defineProps({
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

</script>

<template>
  <div class="divmain">
    <div class="div">
      <label for="name">Nome:</label>
      <input type="text" id="name" v-model="props.name" />

      <label for="email">Email:</label>
      <input type="email" id="email" v-model="props.email" />

      <label for="senha">Senha:</label>
      <input type="password" id="senha" v-model="props.senha" />

      <label for="senhaConfirma">Confirme a senha:</label>
      <input type="password" id="senhaConfirma" v-model="props.senhaConfirma" />

      <label for="nascimento">Data de Nascimento:</label>
      <input type="date" id="nascimento" v-model="props.nascimento" />

      <label for="endereco">Endereço:</label>
      <input type="text" id="endereco" v-model="props.endereco" />

      <label for="cidade">Cidade:</label>
      <input type="text" id="cidade" v-model="props.cidade" />

      <label for="estado">Estado:</label>
      <select id="estado" name="estado">
        <option value="AC">Acre</option>
        <option value="AL">Alagoas</option>
        <option value="AP">Amapá</option>
        <option value="AM">Amazonas</option>
        <option value="BA">Bahia</option>
        <option value="CE">Ceará</option>
        <option value="DF">Distrito Federal</option>
        <option value="ES">Espírito Santo</option>
        <option value="GO">Goiás</option>
        <option value="MA">Maranhão</option>
        <option value="MT">Mato Grosso</option>
        <option value="MS">Mato Grosso do Sul</option>
        <option value="MG">Minas Gerais</option>
        <option value="PA">Pará</option>
        <option value="PB">Paraíba</option>
        <option value="PR">Paraná</option>
        <option value="PE">Pernambuco</option>
        <option value="PI">Piauí</option>
        <option value="RJ">Rio de Janeiro</option>
        <option value="RN">Rio Grande do Norte</option>
        <option value="RS">Rio Grande do Sul</option>
        <option value="RO">Rondônia</option>
        <option value="RR">Roraima</option>
        <option value="SC">Santa Catarina</option>
        <option value="SP">São Paulo</option>
        <option value="SE">Sergipe</option>
        <option value="TO">Tocantins</option>
      </select>

      <label for="hobbies">Hobbies:</label>
      <input type="text" id="hobbies" v-model="props.hobbies" />

      <label for="linguagens">Linguagens de Programação:</label>
      <input type="text" id="linguagens" v-model="props.linguagens" />

      <label for="biografia">Biografia:</label>
      <textarea id="biografia" v-model="props.biografia"></textarea>
    </div>
  </div>
</template>

<style scoped></style>
