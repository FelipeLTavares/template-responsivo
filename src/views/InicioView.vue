<template>
  <div class="hello">
    <CabecalhoGeral/>
    <main>
      <ListaGrupos/>
      <ListaProdutos :lista="produtos"/>
    </main>
    <footer></footer>
  </div>
</template>

<script>
  import ListaProdutos from '@/components/Main/Produtos/ListaProdutos.vue';
  import ListaGrupos from '@/components/Main/Grupos/ListaGrupos.vue';
  import CabecalhoGeral from '@/components/Head/CabecalhoGeral.vue';

  export default {
    name: 'InicioView',
    components: {
    ListaProdutos,
    ListaGrupos,
    CabecalhoGeral
}
  }
</script>

<style scoped>
  .hello{
    display: grid;
    grid-template: 90vh auto 30vh/ auto auto;
    grid-template-areas: 'a a' 'b b' 'c c';
  }
  main{
    background-color: white;
    width: 100%;
    grid-area: b;
  }
  footer{
    background-color: #222831;
    width: 100%;
    grid-area: c;
  }
</style>
