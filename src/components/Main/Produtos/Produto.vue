<template>
  <div class="produto">
    <img :src="produtoImagem" :alt="produtoNome">
    <span class="nome">{{produtoNome}}</span>
    <span class="valor">{{produtoValor}}</span>
  </div>
</template>

<script>
export default {
  name: 'CardProduto',
  props:{
    produtoImagem: String,
    produtoNome: String,
    produtoValor: String
  }
}
</script>

<style scoped>
  .produto{
    width: 280px;
    object-fit: cover;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: start;
  }

  .produto > img{
    min-width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 1px
  }

  .nome, .valor{
    font-size: 15px;
    font-weight: 700;
    align-self: flex-start;
  }
  .valor{
    font-size: 12px;
    font-weight: 400;
  }
</style>