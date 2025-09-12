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
  import Slots from './components/Slots.vue';

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
  <Slots>
    <template v-slot:icone>
      <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-home"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 12l-2 0l9 -9l9 9l-2 0" /><path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" /><path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" /></svg>
    </template>
    <template v-slot:texto>
      Home
    </template>
  </Slots>
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
