<template>
  <div class="bg" id="latestprojects">
    <h1>Latest Project</h1>
    <div class="bgc">
      <Carousel :autoplay="750" :itemsToShow="3.95" :wrapAround="true" :transition="500" :breakpoints="breakpoints">
        <Slide v-for="slide in images" :key="slide">
          <img class="carousel__item" :src="slide" />
        </Slide>
        <!-- <Navigation class="nav" /> -->
        <template #addons>
          <Pagination />
          <!-- <Navigation /> -->
        </template>
      </Carousel>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";
import prj1 from "@/assets/images/webdito.jpg";
import prj2 from "@/assets/images/ampp.jpg";
import prj3 from "@/assets/images/moview.png";
import prj4 from "@/assets/images/webdito.jpg";
import prj5 from "@/assets/images/ampp.jpg";
import prj6 from "@/assets/images/moview.png";
import prj7 from "@/assets/images/webdito.jpg";
import prj8 from "@/assets/images/ampp.jpg";
import prj9 from "@/assets/images/moview.png";

export default defineComponent({
  name: "CarouselComp",
  components: {
    Carousel,
    Slide,
    Pagination,
  },
  data() {
    return {
      images: [prj1, prj2, prj3, prj4, prj5, prj6, prj7, prj8, prj9],
      breakpoints: {
        200: {
          itemsToShow: 1,
          snapAlign: "center",
        },
        500: {
          itemsToShow: 1,
          snapAlign: "center",
        },
        800: {
          itemsToShow: 3,
          snapAlign: "center",
        },
      },
    };
  },
});
</script>

<style scoped>
.bg {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-items: center;
  padding-top: 70px;
  padding-bottom: 100px;
  gap: 3rem;
}

.bgc {
  width: 85%;
  height: auto;
}

.bg h1 {
  font-family: "Montserrat", sans-serif;
  font-size: 60px;
  color: var(--biru);
  margin: auto;
  text-align: center;
}

.carousel__item {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 10px;
}

.carousel__slide {
  padding: 10px;
}

.carousel__viewport {
  perspective: 5000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: 0.5s;
}

.carousel__slide {
  opacity: 0.9;
  transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active ~ .carousel__slide {
  transform: rotateY(20deg) scale(0.9);
}

.carousel__slide--prev {
  opacity: 1;
  transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--next {
  opacity: 1;
  transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--active {
  opacity: 1;
  transform: rotateY(0) scale(1.1);
}
</style>
