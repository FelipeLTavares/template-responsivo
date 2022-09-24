<template>
  <div class="secaoProdutos">
    <h2>Produtos</h2>
    <div class="linha"></div>
    <div class="listaProdutos">
      <CardProdutos v-for="item in listaa" :key="item.nome" :produtoImagem="item.url"
      :produtoNome="item.nome" :produtoValor="item.valor"
      ></CardProdutos>
    </div>
  </div>
</template>

<script>
import CardProdutos from './Produto.vue'

export default {
  name:'ListaProdutos',
  components:{
    CardProdutos
  },
  data(){
    return{
      listaa: [
        {
          url: 'https://i.picsum.photos/id/101/2621/1747.jpg?hmac=cu15YGotS0gIYdBbR1he5NtBLZAAY6aIY5AbORRAngs',
          nome: 'Produto 1',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/102/4320/3240.jpg?hmac=ico2KysoswVG8E8r550V_afIWN963F6ygTVrqHeHeRc',
          nome: 'Produto 2',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/103/2592/1936.jpg?hmac=aC1FT3vX9bCVMIT-KXjHLhP6vImAcsyGCH49vVkAjPQ',
          nome: 'Produto 3',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/104/3840/2160.jpg?hmac=Rv0qxBiYb65Htow4mdeDlyT5kLM23Z2cDlN53YYldZU',
          nome: 'Produto 4',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/67/2848/4288.jpg?hmac=X_Z0Wdd3HiJ8eWT0ohdmpRSIA6e6s265INUMuHA8MqA',
          nome: 'Produto 5',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/45/4592/2576.jpg?hmac=Vc7_kMYufvy96FxocZ1Zx6DR1PNsNQXF4XUw1mZ2dlc',
          nome: 'Produto 6',
          valor: 'R$ 1000,00'
        } ,
        {
          url: 'https://i.picsum.photos/id/104/3840/2160.jpg?hmac=Rv0qxBiYb65Htow4mdeDlyT5kLM23Z2cDlN53YYldZU',
          nome: 'Produto 4',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/67/2848/4288.jpg?hmac=X_Z0Wdd3HiJ8eWT0ohdmpRSIA6e6s265INUMuHA8MqA',
          nome: 'Produto 5',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/45/4592/2576.jpg?hmac=Vc7_kMYufvy96FxocZ1Zx6DR1PNsNQXF4XUw1mZ2dlc',
          nome: 'Produto 6',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/101/2621/1747.jpg?hmac=cu15YGotS0gIYdBbR1he5NtBLZAAY6aIY5AbORRAngs',
          nome: 'Produto 1',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/102/4320/3240.jpg?hmac=ico2KysoswVG8E8r550V_afIWN963F6ygTVrqHeHeRc',
          nome: 'Produto 2',
          valor: 'R$ 1000,00'
        },
        {
          url: 'https://i.picsum.photos/id/103/2592/1936.jpg?hmac=aC1FT3vX9bCVMIT-KXjHLhP6vImAcsyGCH49vVkAjPQ',
          nome: 'Produto 3',
          valor: 'R$ 1000,00'
        }       
      ]
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
    row-gap: 20px;
    padding-top: 30px;
    padding-bottom: 30px;
  }
  .secaoProdutos{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .secaoProdutos > h2{
    margin: 0 0 0 20px;
  }
  .secaoProdutos > .linha{
    height: 1px;
    background-color: gray;
    width: 90%;
    margin-left: 20px;
  }
</style>