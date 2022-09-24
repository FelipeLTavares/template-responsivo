<template>
  <div class="hello">
    <!-- <div class="head">
      <header>
        <div class="headerConteudo">
          <p>FELIPE</p>

          <nav>
            <MenuIcon class="menuicon"></MenuIcon>
            <span>HOME</span>
            <span>ABOUT</span>
            <span>CONTACT</span>
          </nav>
        </div>
      </header>
      <nav v-show="false">
            <span>HOME</span>
            <span>ABOUT</span>
            <span>CONTACT</span>
          </nav>
      <img src="https://i.picsum.photos/id/0/5616/3744.jpg?hmac=3GAAioiQziMGEtLbfrdbcoenXoWAW-zlyEAMkfEdBzQ" alt="Algo">
    </div> -->
    <CabecalhoGeral></CabecalhoGeral>

    <main>
      <ListaGrupos></ListaGrupos>

      <ListaProdutos :lista="produtos"></ListaProdutos>
    </main>
    <footer></footer>
  </div>
</template>

<script>
  /* import MenuIcon from 'vue-material-design-icons/Menu.vue'; */
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
/*   .head{
    background-color:black;
    width: 100%;
    height: 100vh;
    grid-area: a;
  }
  .head > img{
    object-fit: cover;
    width: 100%;
    height: 100vh;
  }
  header{
    width: 100%;
    height: 80px;
    background-color: rgba(238, 238, 238, 0.1);
    display: grid;
    position: absolute;
  }
  .headerConteudo{
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .headerConteudo > p{
    color: white;
    margin: 20px;
    font-size: 40px;
  }
  .headerConteudo > nav{  
    width: 50%;
    display: flex;
    flex-direction: row-reverse;    
  }
  .headerConteudo > nav > span{
    margin: 20px;
    color: white;
  }
  .headerConteudo > nav > span:hover{
    color: orange;
  }
  .headerConteudo > nav > .menuicon {
      display: none;
  } */
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

/*   @media (max-width: 800px){
    .hello{
      grid-template: 50vh auto 30vh/ auto auto;
      grid-template-areas: 'a a' 'b b' 'c c';
    }
    .head{
      height: 50vh;
      width: fit-content;
    }
    .head > img{
      height: 50vh;
    }
    .headerConteudo > nav > span {
      display: none;
    }
    .headerConteudo > nav > .menuicon {
      display: inline;
    }
  }

  @media (max-width: 420px){
    .headerConteudo > nav > span {
      display: none;
    }
    .headerConteudo > nav > .menuicon {
      display: inline;
    }
    .headerConteudo > p{
      color: white;
      font-family: 'Reem Kufi Ink', sans-serif;
      font-size: 30px;
    }
  } */
</style>
