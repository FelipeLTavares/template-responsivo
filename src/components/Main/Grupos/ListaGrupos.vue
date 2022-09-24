<template>
  <div class="secaoGrupos">
    <GrupoProduto v-for="grupo in grupos" :key="grupo.nome" :url="grupo.url" :nome="grupo.nome"></GrupoProduto>
  </div>
</template>

<script>
import GrupoProduto from './GrupoProduto.vue';
export default {
    name: "SecaoGrupos",
    data() {
        return {
            grupos: [
                {
                    nome: "Grupo 1",
                    url: "https://i.picsum.photos/id/996/4272/2848.jpg?hmac=yqRTUY4WFeUSayrtW0dHKMoWx8hd3NQw5TOOKaxZueY"
                },
                {
                    nome: "Grupo 2",
                    url: "https://i.picsum.photos/id/995/3478/2310.jpg?hmac=vKDDYp0DkXNricuHfw_QJgD2VEGWFcrDYhoOXok4a-8"
                },
                {
                    nome: "Grupo 3",
                    url: "https://i.picsum.photos/id/999/4000/2667.jpg?hmac=mTyBy8HWG_rqFam5j6PDtddQR2yBgA_EGhHdzx_SyPw"
                }
            ]
        };
    },
    components: { GrupoProduto }
}
</script>

<style>
  .secaoGrupos{
    width: 100%;
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    padding: 40px 0px;
  }
</style>