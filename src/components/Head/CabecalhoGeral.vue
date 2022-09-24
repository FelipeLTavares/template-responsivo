<template>
  <div class="head">
    <header>
        <p>FELIPE</p>

        <nav>
          <MenuIcon></MenuIcon>
          <span>HOME</span>
          <span>ABOUT</span>
          <span>CONTACT</span>
        </nav>
    </header>
      <nav v-show="false">
        <span>HOME</span>
        <span>ABOUT</span>
        <span>CONTACT</span>
      </nav>
    <img src="https://i.picsum.photos/id/0/5616/3744.jpg?hmac=3GAAioiQziMGEtLbfrdbcoenXoWAW-zlyEAMkfEdBzQ" alt="Algo">
  </div>
</template>

<script>
import MenuIcon from 'vue-material-design-icons/Menu.vue';

export default {
  name: 'CabecalhoGeral',
  components:{
    MenuIcon
  }
}
</script>

<style>
  .head{
    background-color:black;
    width: 100%;
    height: 90vh;
    grid-area: a;
  }
  .head > img{
    object-fit: cover;
    object-position: 50%;
    width: 100%;
    height: 90vh;
  }
  header{
    width: 100%;
    height: 80px;
    background-color: rgba(238, 238, 238, 0.1);
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  header > p{
    color: white;
    margin: 20px;
    font-size: 40px;
  }
  header > nav{  
    width: 50%;
    display: flex;
    flex-direction: row-reverse;    
  }
  header > nav > span{
    margin: 20px;
    color: white;
  }
  header > nav > span:hover{
    color: orange;
  }
  header > nav > .menuicon {
      display: none;
  }
</style>