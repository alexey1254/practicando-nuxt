<template>
    <h1>Bienvenido a la pokeapi!</h1>

    <h3>Busca tu pokemon</h3>
    <p>Pokemon {{ buscarPokemon }}</p> <!--Aquí no me actualiza, no puede leer las propiedades de "null"-->
    <input 
    class="form-text" 
    type="text" 
    v-model="buscarPokemon"
    @keyup="imprimirPokemon()"
    >
    
</template>

<script setup>
const buscarPokemon = ref("")
const pokemon = {
    name:"", // forms.name
    id:"", //id
    image: "", //sprites.official-artwork.front_default
    image_shiny:"" // sprites.official-artwork.front_shiny
}
function imprimirPokemon() {
    console.log(buscarPokemon._value)
}
</script>