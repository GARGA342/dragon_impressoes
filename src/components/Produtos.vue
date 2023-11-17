<template>
  <div class="main_product">
    <h1>Produtos</h1>
    <div class="container">
      <vueper-slides
        class="no-shadow slides"
        :visible-slides="3"
        autoplay
        slide-multiple
        :gap="3"
        :breakpoints="breakpoints"
        :touchable="true"
      >
        <vueper-slide
          class="card"
          v-for="(card, i) in cards"
          :key="i"
        >
          <template #content>
            <div class="vueperslide__content-wrapper">
              <img :src="card.img" class="card_img">
              <p>{{ card.title }}</p>
              <button @click="clickEvent"><span>FAÇA SEU PEDIDO</span></button>
            </div>
          </template>
        </vueper-slide>
      </vueper-slides>
    </div>
  </div>
</template>

<script setup>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

const emit = defineEmits(["clickEvent"]);

const cards = [
 { title: "Porta copos de madeira", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/1.png?raw=true" },
 { title: "Acessórios para decoração", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/2.png?raw=true" },
 { title: "Porta copos de PLA", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/3.png?raw=true" },
 { title: "Acessórios Personalizados", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/4.png?raw=true" },
 { title: "Bustos de personagens", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/5.png?raw=true" },
 { title: "Placas para divulgação de marca", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/6.png?raw=true" },
 { title: "Placas personalizadas", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/7.png?raw=true" },
 { title: "Impressões em resina", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/8.png?raw=true" },
 { title: "Troféus personalizados", img: "https://github.com/GARGA342/dragon_impressoes/blob/master/src/assets/img/cards/9.png?raw=true" },
];

const breakpoints = {
    1215: {
      visibleSlides: 2, slideMultiple: 2
    },
    975: {
      visibleSlides: 1, slideMultiple: 1
    }
  };

function clickEvent() {
  emit("clickEvent", "#pedidos");
}
</script>

<style>
.main_product {
  background-color: #c50018;
  padding: 10px 0 50px 0;
  z-index: 0;
}

.container {
  background-color: #b30016;
  margin-top: 1.5rem;
  padding: 5rem 5rem 2rem 5rem;
}

h1 {
  color: white;
  font-weight: bold;
  margin-inline: 4.69rem;
}

.card {
  display: flex;
  box-sizing: border-box;
  box-shadow: 10px 10px 5px 5px rgba(0, 0, 0, 0.25);
  margin-bottom: 1rem;
  border-radius: 10px;
  background-color: white;
}

.card_img{
  max-width: 60%;
  max-height: 70%;
  border-radius: 5%;
  display: block;
  margin-inline: auto;
  box-shadow: #484848 5px 5px 20px 1px;
}

.vueperslide__content-wrapper button{
  display: flex;
  border-radius: 0.8rem;
  background: #c50018;
  width: 90%;
  height: 10%;
  justify-content: center;
  align-items: center;
  margin-inline: auto;
  margin-top: 15px;
  padding: 0.5rem;
  border: none;
  cursor: pointer;
}

.vueperslide__content-wrapper button span{
  color: white;
  font-weight: 800;
  font-size: 90%;
  font-family: Inter, "Gill Sans", sans-serif;
}

.vueperslide__content-wrapper{
  display: block !important;
  padding-top: 10px;
  text-align: unset !important;
}

.vueperslide__content-wrapper p{
  padding: 1rem 0 0 2rem;
  font-size: large;
}

.vueperslides__parallax-wrapper{
  padding-bottom: calc(120px + 20%) !important;
}

.vueperslides__bullet .default {
  background-color: rgba(0, 0, 0, 0.3);
  border: none;
  box-shadow: none;
  transition: 0.3s;
  width: .7rem;
  height: .7rem;
  transition: .5s;
}

.vueperslides__bullet--active .default {
  background-color: white;
}

.vueperslides__bullet span {
  display: block;
  color: #fff;
  font-size: 10px;
  opacity: 0.8;
}

.vueperslides__arrow {color: white}

@media (max-width: 1215px) {
  .vueperslides__parallax-wrapper{
    padding-bottom: calc(120px + 30%) !important;
  }

  .vueperslides__inner{
    padding: 20px;
  }

}

@media (max-width: 975px) {
  .vueperslides__parallax-wrapper{
    padding-bottom: calc(120px + 70%) !important;
  }

  .vueperslides__inner{
    padding-bottom: 80px;
  }

  .container{
    padding: 0px;
  }

  .vueperslide__content-wrapper span{
    font-size: medium;
  }

  .vueperslides__arrow{
    display: none;
  }
}
</style>