<script>
  import SearchPokemon from './SearchPokemon.vue'
  export default{
    name: 'Main',
    components:{
      SearchPokemon,
    }
  }
</script>

<template>
    <section class="m-5">
        <div class="pokedex">
            <div class="d-flex">
                <div class="col ms-b-r p-2">
                    <SearchPokemon></SearchPokemon>
                </div>
                <div class="col ms-b-l p-2">
                    <SearchPokemon></SearchPokemon>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.pokedex{
    margin: 0 auto;
    width: 70%;
    max-width: 100%;
    border: 20px solid rgb(128, 42, 42);
    border-radius: 20px;
    .ms-b-r{
        border-right: 10px solid rgb(128, 42, 42);
    }
    .ms-b-l{
        border-left: 10px solid rgb(128, 42, 42);
    }
    .col{
        background-color: red;
    }
}
</style>