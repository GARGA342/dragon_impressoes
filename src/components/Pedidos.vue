<template>
  <section class="main">
    <h1>Pedidos</h1>
    <div class="content">
      <div class="social">
        <a class="network" id="wpp">
          <img src="../assets/img/wpp.svg" />
          <div class="background_hover"><span>WhatsApp</span></div>
        </a>
        <a class="network" href="https://www.facebook.com/dragonimpressoes3d" target="_blank"  id="fb">
          <img id="fb" src="../assets/img/fb.svg" />
          <div class="background_hover"><span>Facebook</span></div>
        </a>
        <a class="network" href="https://www.linkedin.com/in/dragon-impressoes-3d/" target="_blank" id="in">
          <img id="in" src="../assets/img/in.svg" />
          <div class="background_hover"><span>LinkedIn</span></div>
        </a>
        <a class="network" href="https://www.instagram.com/dragon_impressoes_3d/" target="_blank" id="insta">
          <img id="insta" src="../assets/img/insta.svg" />
          <div class="background_hover"><span>Instagram</span></div>
        </a>
      </div>
      <div class="float_imgs">
        <img id="f_img1" src="../assets/img/float_image2.png" />
        <img id="f_img2" src="../assets/img/float_image1.png" />
        <img id="f_img3" src="../assets/img/float_image3.png" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.main {
  background: #484848;
  padding: 5.62rem 0 0 0;
  height: 100vh;
}

.content {
  display: flex;
}

.social {
  display: flex;
  margin-top: 3.5rem;
  margin-left: 12rem;
  max-width: 500px;
  background: #484848;
  flex-direction: column;
  gap: 2rem;
  z-index: 1;
}

.social img {
  width: 5.5rem;
  height: 5.5rem;
  cursor: pointer;
  transition: all 2s;
}

.float_imgs {
  display: flex;
  z-index: 0;
  margin-top: 80px;
}

.float_imgs img {
  position: absolute;
  max-width: 400px;
}

#f_img1 {
  right: 30rem;
  margin-top: 12rem;
}

#f_img2 {
  right: 25rem;
  margin-top: -7rem;
}

#f_img3 {
  right: 2rem;
  margin-top: 3rem;
}

h1 {
  color: white;
  font-weight: bold;
  margin-inline: 4.69rem;
}

.background_hover {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 0;
  height: 0;
  margin: 0.68rem 0 0 2rem;
  padding-left: 1rem;
  z-index: -1;
  background-color: white;
  border-radius: 50px;
  transition: width 0.5s;
}

.background_hover span {
  display: none;
}

.network:hover > .background_hover {
  width: 15rem;
  height: 4rem;
}

.network:hover > .background_hover span {
  display: block;
}

.network {
  position: relative;
  display: flex;
  cursor: pointer;
  color: black;
}
</style>
