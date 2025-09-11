<script setup>
  import PrimeiroComponente from './components/PrimeiroComponente.vue';
  import ComDados from './components/ComDados.vue';
  import ComDadosReativosPrimitivos from './components/ComDadosReativosPrimitivos.vue';
  import ComDadosReativosNaoPrimitivos from './components/ComDadosReativosNaoPrimitivos.vue';
  import DataBinding from './components/DataBinding.vue';
  import ComProps from './components/ComProps.vue';
  import EscutaEvento from './components/EscutaEvento.vue';
  import PropriedadesComputadas from './components/PropriedadesComputadas.vue';
  import PropriedadesAssistidas from './components/PropriedadesAssistidas.vue';
  import RenderizacaoCondicional from './components/RenderizacaoCondicional.vue';
  import RenderizacaoListas from './components/RenderizacaoListas.vue';

  const borracha = "borracha"
  const precoBorracha = 3.50
  const funcionarios = [
    {
      "nome": "Erick",
      "idade": 22
    },
    {
      "nome": "Sarah",
      "idade": 22
    },
    {
      "nome": "Erik",
      "idade": 22
    },
    {
      "nome": "Fernanda",
      "idade": 22
    },
    {
      "nome": "Victória",
      "idade": 22
    },
    {
      "nome": "Graziele",
      "idade": 33
    },
    {
      "nome": "Larissa",
      "idade": 22
    },
  ];

</script>

<template>
  <header>Vue</header>
  <RenderizacaoListas nome="Fictícia" :funcionarios="funcionarios" />
  <RenderizacaoCondicional nome="Márcia" :qtde-cachorros="0"/>
  <PropriedadesAssistidas />
  <PropriedadesComputadas />
  <EscutaEvento />
  <ComProps item="Borracha" :preco="2.50"/>
  <ComProps :item="borracha" :preco="precoBorracha"/>
  <DataBinding/>
  <ComDadosReativosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
</template>
