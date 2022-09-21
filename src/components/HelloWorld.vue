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
    <main></main>
    <footer></footer>
  </div>
</template>

<script>
import MenuIcon from 'vue-material-design-icons/Menu.vue'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    MenuIcon
  }
}
</script>

<style scoped>
  .hello{
    display: grid;
    grid-template: 70vh auto 30vh/ auto auto;
    grid-template-areas: 'a a' 'b b' 'c c';
  }
  .head{
    background-color:black;
    width: 100%;
    grid-area: a;
    overflow: hidden;
    display: grid;
    align-items: flex-start;
  }
  .head > img{
    width: 100%;
    object-fit: contain;
    margin-top: -100px;
    position: absolute;
    z-index: 3;
  }
  header{
    width: 100%;
    height: 100px;
    background-color: rgba(238,238,238,0.1);
    z-index: 4;
    display: grid;
  }
  .headerConteudo{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .headerConteudo > p{
    color: white;
    font-family: 'Reem Kufi Ink', sans-serif;
    margin: 20px;
    font-size: 40px;
  }
  .headerConteudo > nav{  
    font-family: 'Reem Kufi Ink', sans-serif;
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
  }
  footer{
    background-color: #222831;
    width: 100%;
    grid-area: c;
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
    }
    .headerConteudo > nav > span {
      display: none;
    }
    .headerConteudo > nav > .menuicon {
      display: inline;
    }
  }
</style>
