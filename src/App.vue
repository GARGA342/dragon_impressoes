<script setup>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Sobre from './components/Sobre.vue'
import Produtos from './components/Produtos.vue'
import Pedidos from './components/Pedidos.vue'
import Rodape from './components/Rodape.vue'
</script>

<template>
  <Navbar />
  <Home />
  <img id="home_div" src="./assets/img/white_div.png">
  <Sobre />
  <img id="about_div" src="./assets/img/red_div.png">
  <Produtos />
  <Pedidos id="pedidos"/>
  <Rodape />
</template>

<style>
  #home_div{
    display: block;
    width: 100%;
    background-color: #484848;
  }

  #about_div{
    display: block;
    width: 100%;
    background-color: white;
  }

  @media (max-width: 1215px) {
    #about_div{
      margin-top: 5rem;
    }
  }
</style>