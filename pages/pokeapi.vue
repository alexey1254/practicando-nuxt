<template>
    <h1>Bienvenido a la pokeapi!</h1>

    <h3>Busca tu pokemon</h3>
    <div class="card text-center mt-3 mb-3 " style="width: 100%;"> <!--Añadir que se vea una vez buscado el pokemon e implementar texto e imagen, id y nombre-->
        <img src="..." class="card-img-top" alt="...">
        <div class="card-body">
        <p class="card-text">Texto pokemon</p>
        </div>
    </div>
    <input 
    class="form-text mt-3" 
    type="text" 
    v-model="inputUsr"
    @keyup.enter="imprimirPokemon()"
    >
</template>

<script setup>

const inputUsr = ref("")


async function searchPokemon() {
try {
    let data = useFetch(`https://pokeapi.co/api/v2/pokemon/${inputUsr.value}`, {
        pick: ["id", "name", "sprites"]
    })
    return data;
} catch (error) {
    console.log("Error funcion searchPokemon() -> ")
}
}

async function imprimirPokemon() { // Implementar texto del pokemon
    let datos = await searchPokemon();
    this.pokemon.name = datos.data.value.name;
    this.pokemon.id = datos.data.value.id;
    this.pokemon.imagen = datos.data.value.sprites.front_default;
    

}
</script>