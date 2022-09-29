<template>
  <div class="secaoProdutos">
    <h2>Produtos</h2>
    <div class="linha"></div>
    <div class="listaProdutos">
      <CardProdutos v-for="item in produtos" :key="item.nome" :produtoImagem="item.url"
      :produtoNome="item.nome" :produtoValor="item.valor"
      ></CardProdutos>
    </div>
  </div>
</template>

<script>
import CardProdutos from './Produto.vue';
import produtos from './Lista';

export default {
  name:'ListaProdutos',
  components:{
    CardProdutos
  },
  data(){
    return{
      produtos: produtos
    }
  }
}
</script>
  
<style>
  .listaProdutos{
    width: 100%;
    min-height: 500px;
    display: grid;
    grid-template-columns: auto auto auto;
    justify-items: center;
    align-items: center;
    margin-top: 30px;
    margin-bottom: 60px;
  }
  .secaoProdutos{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .secaoProdutos > h2{
    margin: 0 0 0 4%;
  }
  .secaoProdutos > .linha{
    height: 1px;
    background-color: gray;
    width: 90%;
    margin-left: 4%;
  }

  @media(max-width:880px){
    .listaProdutos{
      grid-template-columns: auto auto;
    }
  }

  @media(max-width:600px){
    .listaProdutos{
      grid-template-columns: auto;
    }
  }
</style>