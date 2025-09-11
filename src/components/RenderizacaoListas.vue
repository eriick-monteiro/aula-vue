<template>
    <div class="componente">
        <h1>Componente Rendereização de Lista</h1>
        <p>Empresa: {{ nome }}</p>
        <p v-show="funcionarios.length === 0" >Não tem funcionário</p>
        <p>Os nomes e idades dos funcionarios são:</p>
        <ul>
            <li v-for="funcionario in funcionarios">
                Nome: {{ funcionario.nome }} | Idade: {{ funcionario.idade }}
            </li>
        </ul>
    </div>
</template>


<script setup>
    import { defineProps } from 'vue';

    defineProps({
        nome: String,
        funcionarios: Array
    });
</script>

<style scoped>
    ul {
        margin: 0px;
        padding: 0px;
    }

    li {
        list-style: none;
        text-align: center;
        font-size: large;
    }
</style>