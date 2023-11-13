<template>
  <section class="main">
    <h1>Pedidos</h1>
    <div class="content">
      <div class="social">
        <a class="network" id="wpp">
          <img src="../assets/img/wpp.svg" />
          <div class="background_hover"><span>WhatsApp</span></div>
        </a>
        <a
          class="network"
          href="https://www.facebook.com/dragonimpressoes3d"
          target="_blank"
          id="fb"
        >
          <img id="fb" src="../assets/img/fb.svg" />
          <div class="background_hover"><span>Facebook</span></div>
        </a>
        <a
          class="network"
          href="https://www.linkedin.com/in/dragon-impressoes-3d/"
          target="_blank"
          id="in"
        >
          <img id="in" src="../assets/img/in.svg" />
          <div class="background_hover"><span>LinkedIn</span></div>
        </a>
        <a
          class="network"
          href="https://www.instagram.com/dragon_impressoes_3d/"
          target="_blank"
          id="insta"
        >
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
  position: absolute;
  display: grid;
  gap: 20px;
  grid-template-columns: auto auto auto;
  max-height: 80vh;
  right: 0;
  z-index: 0;
}

#f_img1,
#f_img2,
#f_img3 {
  max-width: 80%;
}

#f_img1 {
  grid-column: 1 / 3;
  grid-row-start: 2;
}

#f_img2 {
  grid-column: 2 / 4;
  grid-row-start: 1;
}

#f_img3 {
  grid-column: 3 / 4;
  grid-row-start: 2;
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

@media (max-width: 1215px) {
  .float_imgs {
    max-width: 600px;
  }

  .social {
    margin-top: 3.5rem;
    margin-left: 5rem;
    gap: 2rem;
  }

  .social img {
    width: 4.5rem;
    height: 4.5rem;
  }

  .network:hover > .background_hover {
    width: 12rem;
    height: 3rem;
  }
}

@media (max-width: 975px) {
  .background_hover {
    z-index: 0;
  }
  .social img {
    z-index: 1;
  }

  .social{
    max-width: unset;
  }

  .main {
    height: 200vh;
  }
  .content {
    display: block;
  }
  .float_imgs {
    display: block;
    right: unset;
    width: auto;
    margin: 3rem auto auto 5rem;
  }

  #f_img1,
  #f_img2,
  #f_img3 {
    max-width: 60%;
    margin-bottom: 2rem;
  }

  .background_hover {
    width: 90%;
    height: 3rem;
    margin-inline: auto;
    z-index: 0;
    background-color: white;
    border-radius: 50px;
  }

  .network:hover > .background_hover {
    width: 95%;
    height: 3rem;
  }

  .background_hover span {
    display: flex;
  }
}
</style>
