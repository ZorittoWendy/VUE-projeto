<template>
    <div class="componente">
        <h1>Componente com Propriedade computadas</h1>
        <p>Idade: {{ idade }}</p>
        <label>Ano de Nascimente:</label>
        <input type="number" v-model="anoNascimento" min="1900">
        <label>Ano Atual:</label>
        <input type="number" v-model="anoAtual" min="1900">
    </div>
</template>
<script setup>
import {ref, computed} from 'vue';
const anoNascimento = ref(1900)
const anoAtual = ref(2000)
const idade = computed(()=>{
    return anoAtual.value - anoNascimento.value
}) 
</script>

<style scoped>
label{
    margin: 10px;
}
</style>