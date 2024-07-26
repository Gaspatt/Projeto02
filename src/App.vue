<script setup>
import FormInicial from './components/FormInicial.vue'
import FormResp from './components/FormResp.vue'

import { ref } from 'vue'

const mostrarResultado = ref(false)

const dados = ref({})

function mostrar(data) {
    mostrarResultado.value = true
    dados.value = data
}

</script>

<template>
    <FormInicial v-if="!mostrarResultado" @enviar="mostrar"/>
    <FormResp v-if="mostrarResultado" :dados="dados"/>
</template>

<style scoped></style>
