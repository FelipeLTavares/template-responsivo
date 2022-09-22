<template>
  <div class="hello">
    <div class="head">
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
      <img src="https://i.picsum.photos/id/0/5616/3744.jpg?hmac=3GAAioiQziMGEtLbfrdbcoenXoWAW-zlyEAMkfEdBzQ" alt="Algo">
    </div>
    <main>
      <div class="sessaoGrupos">
        <GrupoProduto id="grupo1"></GrupoProduto>
        <GrupoProduto id="grupo2"></GrupoProduto>
        <GrupoProduto id="grupo3"></GrupoProduto>
      </div>
    </main>
    <footer></footer>
  </div>
</template>

<script>
import MenuIcon from 'vue-material-design-icons/Menu.vue';
import GrupoProduto from './GrupoProduto.vue';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    GrupoProduto,
    MenuIcon
  }
}
</script>

<style scoped>
  .hello{
    display: grid;
    grid-template: 90vh auto 30vh/ auto auto;
    grid-template-areas: 'a a' 'b b' 'c c';
  }
  .head{
    background-color:black;
    width: 100%;
    height: 90vh;
    grid-area: a;
  }
  .head > img{
    object-fit: cover;
    width: 100%;
  }
  header{
    width: 100%;
    height: 80px;
    background-color: rgba(238,238,238,0.1);
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
    }
  main{
    background-color: white;
    width: 100%;
    height: 400px;
    grid-area: b;
    display: grid;
  }
  footer{
    background-color: #222831;
    width: 100%;
    grid-area: c;
  }

  .sessaoGrupos{
    margin-top: 60px;
    width: 100%;
    height: 350px;
    display: grid;
    grid-template-columns: auto auto auto;
    justify-content: space-evenly;
  }
  @media (max-width: 800px){
    .head > img{
      height: 90vh;
      min-width: 100%;
    }
    .headerConteudo > nav > span {
      display: none;
    }
    .headerConteudo > nav > .menuicon {
      display: inline;
    }

    .sessaoGrupos{
      grid-template-columns: auto auto;
    }
  }

  @media (max-width: 420px){
    .head{
      height: 60vh;
    }
    .head > img{
      margin-top: 0px;
      margin-left: -150px;
      height: 60vh;
      width: 200%;
      object-fit: contain;
    }
    header{
      height: 60px;
    }
    .headerConteudo{
      height: 60px;
    }
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
  }
</style>
