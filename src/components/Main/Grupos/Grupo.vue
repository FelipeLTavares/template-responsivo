<template>
  <div class="grupo">
    <img :src="url" :alt="nome">
    <div class="descricaoGrupo">
      <h2>{{nome}}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GrupoProduto',
  props:{
    url: String,
    nome: String
  }
}
</script>

<style>
  .grupo{
    width: 70%;
    min-width: 200px;
    height: 200px;
    position: relative;
    margin: 30px 0;
  }
  .grupo > img{
    object-fit: cover;
    height: 200px;
    width: 100%;
    border-radius: 5px;
  }
  .grupo > img:hover{
    opacity: 0.9;
  }
  .descricaoGrupo{
    width: 50%;
    position: absolute;
    top: 0;
    color: white;
  }
</style>