<script setup></script>

<template>
  <form class="main-container">
    <div class="main-cointer-title">Компания <span>«Мастера ремонта»</span> в Москве</div>
    <div class="main-container-description">
      Сделаем качественный ремонт квартиры под ключ.<span>Расширенная гарантия до 3х лет.</span>
      Подбор, закупка и доставка материала.
    </div>
    <div class="submission-form">
      <input
        class="submission-form-accuracy"
        placeholder="Введите Ваш номер телефона"
        type="tel"
        id="phone"
        name="phone"
        pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}"
        required
      />
      <button class="btn">Заказать звонок</button>
    </div>
  </form>
</template>

<style scoped>
.btn {
  background: #003998;
  color: #fff;
  font-size: 14px;
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.25);
  border-radius: 60px;
  cursor: pointer;
  width: 235px;
  height: 60px;
}
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
.submission-form {
  display: flex;
  justify-content: space-between;
  width: 100%;
  /* height: 62px; */
  background: #202020;
  border: 1px solid #818181;
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.25);
  border-radius: 60px;
  margin-bottom: 40px;
}
.submission-form-accuracy {
  border: none;
  background: transparent;
  flex: 1;
  padding-left: 20px;
  color: rgba(255, 255, 255, 0.7);
}

.submission-form-accuracy:focus-visible {
  border: 0;
  outline: none;
}
.submission-form .btn {
  flex-shrink: 0;
  flex-grow: 0;
  border: none;
}

@media (max-width: 1085px) {
  .submission-form {
    display: block;
    border: 0;
    background: transparent;
    box-shadow: none;
  }
  .main-container-description {
    margin-bottom: 20px;
  }
  .submission-form > * {
    display: block;
  }
  .submission-form input {
    background: #202020;
    border: 1px solid #818181;
    box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.25);
    border-radius: 60px;
    width: 100%;
    height: 60px;
    margin-bottom: 6px;
  }
  .main-cointer-title {
    font-size: 20px;
  }
  .main-container-description {
    font-size: 14px;
  }

  .submission-form .btn {
    width: 100%;
    border: none;
  }
}
</style>
