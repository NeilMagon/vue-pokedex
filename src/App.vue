<script>
  import Main from './components/Main.vue'
  export default{
    components:{
      Main,
    }
  }
</script>

<template>
  <div class="text-center m-2">
    <h1>PokeVue</h1>
  </div>
  <Main></Main>
</template>

<style lang="scss" scoped>
h1{
  font-size: 4rem;
  font-weight: 800;
  background: linear-gradient(to right, red, blue);
  background-clip: text;
  color: transparent;
}
</style>
