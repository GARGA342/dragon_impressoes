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
        :slide-ratio="1 / 4"
        :dragging-distance="200"
        :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }"
      >
        <vueper-slide
          class="card"
          v-for="(card, i) in cards"
          :key="i"
        >
          <template #content>
            <div
              class="vueperslide__content-wrapper"
            >
              <img :src="card.img" class="card_img">
              <p>{{ card.title }}</p>
              <button><span>FAÇA SEU PEDIDO</span></button>
            </div>
          </template>
        </vueper-slide>
      </vueper-slides>
    </div>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

export default {
  components: {
    VueperSlides,
    VueperSlide,
  },
  data() {
    return {
      cards: [
        { title: "EXEMPLO", img: "../src/assets/img/cards/1.jpg" },
        { title: "EXEMPLO", img: "../src/assets/img/cards/2.jpg" },
        { title: "EXEMPLO", img: "../src/assets/img/cards/3.jpg" },
        { title: "EXEMPLO", img: "../src/assets/img/cards/4.jpg" },
        { title: "EXEMPLO", img: "../src/assets/img/cards/4.jpg" },
      ],
    };
  },
};
</script>

<style>
.main_product {
  background-color: #c50018;
  padding: 10px 0 50px 0;
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
  max-width: 80%;
  border-radius: 5%;
  display: block;
  margin-inline: auto;
  box-shadow: #484848 5px 5px 20px 1px;
}

.vueperslide__content-wrapper button{
  display: block;
  border-radius: 0.8rem;
  background: #c50018;
  width: 90%;
  margin-inline: auto;
  margin-top: 15px;
  padding: 0.5rem;
  border: none;
  cursor: pointer;
}

.vueperslide__content-wrapper button span{
  color: white;
  font-weight: 800;
  font-family: Inter;
}

.vueperslide__content-wrapper{
  display: block !important;
  padding-top: 10px;
  text-align: unset !important;
}

.vueperslide__content-wrapper p{
  padding: 1rem 0 0 2rem;
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
</style>