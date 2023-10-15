<template>
  <section class="main">
    <h1>Produtos</h1>
    <div class="content">
      <button class="prev-button"></button>
      <div class="carousel-container">
        <div class="carousel">
          <div class="slide">
            <img src="../assets/img/cards/1.jpg" alt="Imagem 1" class="card_img"/>
            <p class="card_p">Porta copos de madeira</p>
            <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
          </div>
          <div class="slide">
            <img src="../assets/img/cards/2.jpg" alt="Imagem 2" class="card_img"/>
            <p class="card_p">Artigos para decoração</p>
            <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
          </div>
          <div class="slide">
            <img src="../assets/img/cards/3.jpg" alt="Imagem 3" class="card_img"/>
            <p class="card_p">Porta copos em PLA</p>
            <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
          </div>
          <div class="slide">
            <img src="../assets/img/cards/3.jpg" alt="Imagem 4" class="card_img"/>
            <p class="card_p">EXEMPLO</p>
            <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
          </div>
          <div class="slide">
            <img src="../assets/img/cards/3.jpg" alt="Imagem 4" class="card_img"/>
            <p class="card_p">EXEMPLO</p>
            <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
          </div>
        </div>
      </div>
      <button class="next-button"></button>
    </div>
  </section>
</template>

<style scoped>
.main {
  background-color: #c50018;
  min-height: 85vh;
}

h1 {
  color: white;
  font-weight: bold;
  margin-inline: 4.69rem;
}

.carousel-container {
  overflow: hidden;
  width: 1200px;
  margin-inline: auto;
}

.content {
  display: flex;
  align-items: center;
  background: rgba(132, 0, 16, 0.28);
  margin-top: 20px;
}

.carousel {
  display: flex;
  transition: transform 0.3s;
}

.slide {
    flex: 0 0 calc(100% / 4);
    overflow: hidden;
    border: 1px solid #484848;
    border-radius: 10px;
    padding: 20px 30px;
    margin: 1rem 1.2rem 1.6rem 1.2rem;
    box-shadow: 10px 10px 10px 10px rgba(0, 0, 0, 0.25);
    background-color: white;
}

.card_img {
  max-width: 300px;
  display: block;
  margin-top: 10px;
  box-shadow: #484848 5px 5px 20px 1px;
  border-radius: 10px;
}

.card_p {
  display: block;
  margin-top: 30px;
  margin-left: .7rem;
}

.btn_pedido {
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

.btn_pedido span {
  color: white;
  font-weight: 800;
  font-family: Inter;
}

.next-button{
    height: 80px;
    width: 80px;
    background: no-repeat center/80% url("../assets/img/right_arrow.svg");
    border: none;
    cursor: pointer;
    margin-inline: auto;
}

.prev-button{
    height: 80px;
    width: 80px;
    background: no-repeat center/80% url("../assets/img/left_arrow.svg");
    border: none;
    cursor: pointer;
    margin-inline: auto;
    transition: transform 0.3s;
}

.prev-button:active, .next-button:active{
  transform: translateY(10px);
}
</style>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const carousel = document.querySelector(".carousel");
  const slides = document.querySelectorAll(".slide");

  let currentIndex = 0;
  const slideWidth = slides[0].clientWidth;
  const numVisibleSlides = 3;
  let intervalTime = 3000;

  function updateCarousel() {
    const offset = currentIndex * (slideWidth + 40);
    carousel.style.transform = `translateX(-${offset}px)`;
  }

  function nextSlide() {
    currentIndex = (currentIndex + 1) % (slides.length - numVisibleSlides + 1);
    intervalTime = 3000;
    updateCarousel();
  }

  function prevSlide() {
    currentIndex =
      (currentIndex - 1 + (slides.length - numVisibleSlides + 1)) %
      (slides.length - numVisibleSlides + 1);
      intervalTime = 3000;
    updateCarousel();
  }

  function autoNextSlide() {
    nextSlide();
  }

  document.querySelector(".next-button").addEventListener("click", nextSlide);
  document.querySelector(".prev-button").addEventListener("click", prevSlide);

  setInterval(autoNextSlide, intervalTime);
});
</script>