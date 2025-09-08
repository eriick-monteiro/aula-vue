<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        <button @click="mostrarNomeCompleto">Mostrar Nome Completo</button>
        <button @click="fazerAniversario">Fazer Aniversário</button>
    </div>
</template>

<script setup>
    import {reactive} from "vue";

    const pessoa = reactive({nome: "Erick", idade: 22});

    function fazerAniversario() {
        pessoa.idade += 1;
    }

    function mostrarNomeCompleto() {
        if (pessoa.nome === "Erick") {
            pessoa.nome = "Erick Monteiro dos Anjos";
        } else if (pessoa.nome === "Erick Monteiro dos Anjos") {
            pessoa.nome = "Erick";
        } else {
            pessoa.nome = "Como você fez isso?";
        }
    }
</script>
