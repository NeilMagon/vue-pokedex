<script>
    import axios from 'axios'
    export default{
        name: 'SearchPokemon',
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
</template>

<style lang="scss" scoped>

</style>