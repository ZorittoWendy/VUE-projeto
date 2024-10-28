<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario">Fazer Aniversario</button>
        <button @click="mudarNome()">Mudar nome</button>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const nome = ref('Ana')
const idade = ref(32)
function fazerAniversario() {
    idade.value += 1
}
function mudarNome() {
    nome.value = 'Ana Maria'
}
</script>