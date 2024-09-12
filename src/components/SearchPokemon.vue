<script>
    import axios from 'axios'
    import PokemonDetails from './PokemonDetails.vue'
    export default{
        name: 'SearchPokemon',
        components: {
            PokemonDetails
        },
        data() {
            return {
                pokemonName: '',
            }
        },
        methods: {
            searchPokemon() {
                axios.get(`https://pokeapi.co/api/v2/pokemon/${this.pokemonName.toLowerCase()}`)
                .then(response => {
                    console.log(response.data);
                })
                .catch(error => {
                    console.error('Pokémon non trovato!', error);
                });
            }
        }
    }
</script>

<template>
    <input v-model="pokemonName" placeholder="Cerca un pokemon">
    <button @click="searchPokemon">Cerca</button>
    <PokemonDetails></PokemonDetails>
</template>

<style lang="scss" scoped>

</style>