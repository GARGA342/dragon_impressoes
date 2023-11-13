<template>
  <div class="nav_body">
    <a @click="scrollEvent('#home')"
      ><img src="../assets/img/nav_logo.png" class="nav_logo" alt="Logo da empresa"
    /></a>

    <nav class="nav_links">
      <img class="hamburguer_logo" @click="hamburger_menu" :src="src" />
      <menu>
        <a @click="scrollEvent('#inicio')">Inicio</a>
        <a @click="scrollEvent('#home_div')">Sobre</a>
        <a @click="scrollEvent('#about_div')">Produtos</a>
        <a @click="scrollEvent('#pedidos')">Pedidos</a>
      </menu>
    </nav>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const emit = defineEmits(["scrollEvent"]);
let src = ref('../src/assets/img/nav_icon.svg')

function hamburger_menu() {
  let element = document.querySelector('.nav_links')
  if(element.classList.contains('active')){
    element.classList.remove('active')
    src.value = '../src/assets/img/nav_icon.svg'
  }else{
    element.classList.add('active')
    src.value = '../src/assets/img/cross.svg'
  }
}

function scrollEvent(id) {
  if(id === '#home'){
    emit("scrollEvent", '#inicio');
  }else{
    emit("scrollEvent", id);
    hamburger_menu()
  }
}
</script>

<style scoped>
.nav_body {
  position: fixed;
  background-color: #c50018;
  width: 100%;
  height: 4em;
  display: flex;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  align-items: center;
  justify-content: space-between;
  z-index: 3;
}

.hamburguer_logo {
  position: relative;
  display: none;
  right: 20px;
  background-repeat: no-repeat;
  cursor: pointer;
  width: 30px;
  height: 24px;
}

.nav_links {
  display: contents;
}

.nav_links menu {
  display: flex;
  margin-right: 20px;
  gap: 10px;
  align-items: center;
}

menu a {
  text-decoration: none;
  color: white;
  font-family: Inter;
  cursor: pointer;

}

.nav_links a:hover {
  color: #ffae03;
}

.nav_logo {
  padding: 10px;
  width: 50px;
  cursor: pointer;
}

@media (max-width: 768px) {
  .nav_links menu {
    position: absolute;
    top: 8vh;
    right: 0;
    margin-right: unset !important;
    width: 50vw;
    height: 96vh;
    background-color: #c50018;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    transform: translateX(100%);
    transition: .2s ease-in;
    z-index: 3;
  }

  .active menu{
    transform: translateX(0);
  }

  menu a{
    cursor: pointer;
  }

  .hamburguer_logo {
    display: block;
  }
}
</style>
