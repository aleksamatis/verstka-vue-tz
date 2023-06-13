<script setup></script>

<template>
  <div class="main-container">
    <div class="main-cointer-title">Компания <span>«Мастера ремонта»</span> в Москве</div>
    <div class="main-container-description">
      Сделаем качественный ремонт квартиры под ключ.<span>Расширенная гарантия до 3х лет.</span>
      Подбор, закупка и доставка материала.
    </div>
  </div>
</template>

<style scoped>
.main-cointer-title {
  font-size: 40px;
  color: #fff;
  text-transform: uppercase;
  font-family: 'Prosto One';
  margin-bottom: 25px;
  line-height: 49px;
}
.main-cointer-title span {
  background: linear-gradient(
    268.54deg,
    rgba(33, 104, 222, 0.92) 7.7%,
    rgba(24, 155, 211, 0.86) 100.72%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-fill-color: transparent;
  line-height: 49px;
}

.main-container-description {
  font-size: 16px;
  line-height: 18.75px;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 25px;
  line-height: 19px;
  font-weight: 400;
}

.main-container-description span {
  color: #fff;
  line-height: 19px;
  font-weight: 400;
}

@media (max-width: 1085px) {
  .main-container-description {
    margin-bottom: 20px;
  }
  .main-cointer-title {
    font-size: 20px;
  }
  .main-container-description {
    font-size: 14px;
  }
}
</style>
