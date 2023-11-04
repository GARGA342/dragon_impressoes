<template>
  <div class="main_product">
    <vueper-slides
      class="no-shadow"
      :visible-slides="3"
      slide-multiple
      :gap="3"
      :slide-ratio="1 / 4"
      :dragging-distance="200"
      :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }"
    >
      <vueper-slide class="card" v-for="i in 10" :key="i" :title="i.toString()" />
    </vueper-slides>
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
        { name: "Card 1" },
        { name: "Card 2" },
        { name: "Card 3" },
        { name: "Card 4" },
        { name: "Card 5" },
      ],
    };
  },
};
</script>

<style>
.card {
  text-align: center;
  border: 1px solid #ccc;
  color:white;
  padding: 20px;
  box-sizing: border-box;
}

.default{
  box-shadow: 0 0 1px #484848,0 0 1px #484848 !important;
  background-color: white !important;
}

.vueperslides__bullet--active .default{
  color: #484848;
  border-width: 5px;
}

.vueperslides__arrows--outside{
  color: white;
}

.main_product {
  background-color: brown;
  padding: 100px;
}
</style>
