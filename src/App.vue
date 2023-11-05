<script setup>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import Sobre from "./components/Sobre.vue";
import Produtos from "./components/Produtos.vue";
import Pedidos from "./components/Pedidos.vue";
import Rodape from "./components/Rodape.vue";

function scrollEvent(id){
 const section = document.querySelector(id);
 if (section) {
   section.scrollIntoView({
     behavior: "smooth",
     block: "start",
   });
 }
}
</script>

<template>
 <Navbar v-on:scroll-event="scrollEvent" />
 <Home />
 <img id="home_div" src="./assets/img/white_div.png" />
 <Sobre />
 <img id="about_div" src="./assets/img/red_div.png" />
 <Produtos v-on:click-event="scrollEvent" />
 <Pedidos id="pedidos" />
 <Rodape />
</template>

<style>
#home_div {
  display: block;
  width: 100%;
  background-color: #484848;
}

#about_div {
  display: block;
  width: 100%;
  background-color: white;
}
</style>