<template>
  <div class="grupo">
    <img src="https://i.picsum.photos/id/995/3478/2310.jpg?hmac=vKDDYp0DkXNricuHfw_QJgD2VEGWFcrDYhoOXok4a-8" alt="algo">
    <div class="descricaoGrupo">
      <h2>Grupo 1</h2>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
  .grupo{
    width: 250px;
    height: 200px;
    position: relative;
  }
  .grupo > img{
    object-fit: cover;
    height: 200px;
    width: 100%;
    border-radius: 20px;
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