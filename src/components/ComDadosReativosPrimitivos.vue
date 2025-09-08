<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mostrarNomeCompleto">Mostrar Nome Completo</button>
    </div>
</template>
 dos Anjos
 
<script setup>
    import {ref} from "vue";

    const nome = ref("Erick")
    const idade = ref(22)

    function fazerAniversario() {
        idade.value += 1;
    }

    function mostrarNomeCompleto() {
        if (nome.value === "Erick") {
            nome.value = "Erick Monteiro dos Anjos";
        } else if (nome.value === "Erick Monteiro dos Anjos") {
            nome.value = "Erick";
        } else {
            nome.value = "Como você fez isso?";
        }
    }
</script>
