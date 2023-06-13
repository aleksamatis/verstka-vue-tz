<script setup>
import { ref } from 'vue'

const itemIndex = ref(0)
const carousel = ref()
</script>
<template>
  <div class="main-container">
    <div class="main-container-transformed-2"></div>
    <div class="main-container-transformed"></div>
    <div class="main-gallery">
      <div>
        <el-carousel
          class="main-gallery-carousel"
          indicator-position="outside"
          :initial-index="0"
          @change="itemIndex = $event + 1"
          :autoplay="false"
          arrow="never"
          ref="carousel"
        >
          <el-carousel-item v-for="item in 4" :key="item">
            <img class="gallery-image" src="@/assets/images/image1.jpg" alt="" />
          </el-carousel-item>
        </el-carousel>
        <div class="carousel-buttons">
          <img src="@/assets/images/arrowleft.svg" @click="carousel.prev()" />
          <img src="@/assets/images/ellipse.svg" />
          <img src="@/assets/images/arrow.svg" @click="carousel.next()" />
        </div>
      </div>
      <div class="description-gallery-counter">
        <div>
          <div class="title">Дизайнерский ремонт</div>
          <div class="description">ЖК «Пироговская Ривьера», 104 м²</div>
        </div>
        <div class="gallery-counter">
          <span class="gallery-counter-changed">{{ itemIndex }}</span
          ><span class="gallery-counter-number">/4</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  position: relative;
}

.main-gallery {
  padding: 25px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 40px;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.main-gallery-carousel {
  flex-grow: 1;
  aspect-ratio: 1.1;
}

.carousel-buttons {
  position: absolute;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 80px;
  height: 30px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 60px;
  bottom: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
}

.carousel-buttons img {
  padding: 10px;
}
.main-gallery div.title {
  color: #fff;
  font-family: 'Prosto One';
  font-style: normal;
  font-weight: 400;
  font-size: 25px;
  line-height: 31px;
  text-transform: capitalize;
  text-align: left;
}
.main-gallery div.description {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  color: rgba(255, 255, 255, 0.7);
  display: flex;
}
.main-gallery div.gallery-counter {
  font-family: 'Prosto One';
  color: #fff;
}
.description-gallery-counter {
  display: flex;
  justify-content: space-between;
}
.gallery-counter-changed {
  font-size: 35px;
}

.gallery-counter-number {
  color: #c3c3c3;
}

::v-deep(.el-carousel) {
  display: flex;
  flex-direction: column;
  position: relative;
}

::v-deep(.el-carousel__container) {
  flex-grow: 1;
}

::v-deep(.el-carousel__item) {
  border-radius: 40px;
}
.main-container-transformed {
  height: 516px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 40px;
  transform: rotate(10.46deg);
  position: absolute;
  top: 30px;
  left: 60px;
  width: 100%;
  height: 100%;
}

.main-container-transformed-2 {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(5px);
  border-radius: 40px;
  transform: rotate(19.61deg);
  position: absolute;
  top: 60px;
  left: 90px;
  width: 100%;
  height: 100%;
}

.gallery-image {
  width: 100%;
  height: auto;
}

@media (max-width: 1085px) {
  .main-container {
    width: 100%;
  }
}
</style>
