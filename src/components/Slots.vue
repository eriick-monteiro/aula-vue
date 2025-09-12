<template>
    <div class="componente">
        <h1>Componente com Slots</h1>
        <button>
            <slot name="icone"/>
            <slot name="texto">
                Botão <!-- Esse seria o valor padrão se nada for passado -->
            </slot>
        </button>
    </div>
</template>