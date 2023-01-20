<template>
    <h1>Bienvenido a la pokeapi!</h1>

    <h3>Busca tu pokemon</h3>
    <p>Pokemon {{ buscarPokemon }}</p>
    <input 
    class="form-text" 
    type="text" 
    v-model="buscarPokemon"
    >
    
</template>

<script setup>

const pokemon = {
    name:"", // forms.name
    id:"", //id
    image: "", //sprites.official-artwork.front_default
    image_shiny:"" // sprites.official-artwork.front_shiny
}

</script>