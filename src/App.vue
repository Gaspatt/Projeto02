<script setup>
import FormInicial from './components/FormInicial.vue'
import FormResp from './components/FormResp.vue'
</script>

<template>
  <form class="form" @submit.prevent="submit">
    <div class="h1">
      <h1>Formulário de Cadastro</h1>
    </div>

    <FormInicial />
    <button type="submit">Enviar</button>
  </form>
</template>

<style scoped></style>
