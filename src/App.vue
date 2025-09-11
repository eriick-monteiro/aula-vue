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

  const borracha = "borracha"
  const precoBorracha = 3.50
</script>

<template>
  <header>Vue</header>
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
