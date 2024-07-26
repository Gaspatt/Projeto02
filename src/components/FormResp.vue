<script setup>

defineProps ({
   dados: Object
})
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
        <input id="voltar" type="submit" value="Voltar" @click="voltar">
        
    </div>
</template>

<style scoped>

</style>