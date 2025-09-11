<template>
    <div class="componente">
        <h1>Componente Renderização Condicional</h1>
        <p>Nome: {{ nome }}</p>
        <p v-if="qtdeCachorros === 0">Não tem Cachorros</p>
        <p v-else-if="qtdeCachorros === 1">Tem um Cachorro</p>
        <p v-else="qtdeCachorros > 1">Tem Muitos Cachorros</p>
    </div>
</template>


<script setup>
    import { defineProps } from 'vue';

    defineProps({
        nome: String,
        qtdeCachorros: Number
    });
</script>