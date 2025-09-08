<template>
    <div class="componente">
        <h1>Componente com dados</h1>
        <p>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
    </div>
</template>

<script setup>
    const nomeProduto = "Apontador"
    const codigoProduto = "#987"
</script>

<!-- <script>
    // Options API
    // export default {
    //     data: () => {
    //         return {
    //             nomeProduto: "Caderno",
    //             codigoProduto: "#321"
    //         }
    //     }
    // }

    // Composition API
    // export default {
    //     setup: () => {
    //         const nomeProduto = "Lápis"
    //         const codigoProduto = "#789"

    //         return {
    //             nomeProduto,
    //             codigoProduto
    //         }
    //     }
    // }
</script> -->