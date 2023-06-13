<template>
  <div class="main-menu">
    <div class="main-menu-content">
      <div><img src="@/assets/images/logo.svg" alt="" /></div>
      <div>Ремонт</div>
      <div>Портфолио</div>
      <div>Отзывы</div>
      <button class="btn-header">Заказать звонок</button>
    </div>
  </div>
  <div class="main-menu-small">
    <div class="main-menu-content-small">
      <div><img src="@/assets/images/logosmall.svg" alt="" /></div>
      <div class="roundphone"><img src="@/assets/images/roundphone.svg" alt="" /></div>
      <div class="baselinemenu"><img src="@/assets/images/baselinemenu.svg" alt="" /></div>
    </div>
  </div>
</template>

<style scoped>
.main-menu {
  color: rgba(255, 255, 255, 0.7);
  font-size: 14px;
  padding: 40px 0;
}

.main-menu-content {
  max-width: 1170px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.main-menu div {
  cursor: pointer;
}

.btn-header {
  background: transparent;
  color: #fff;
  font-size: 14px;
  border-radius: 60px;
  border: 2px solid #2168de;
  cursor: pointer;
  width: 280px;
  height: 60px;
}
.roundphone {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 35px;
  height: 35px;
  background: linear-gradient(132.92deg, #1c6cd1 9.16%, #0b74a8 87.83%);
  border-radius: 60px;
  cursor: pointer;
}
.roundphone img {
  width: 21px;
  height: 21px;
}
.baselinemenu {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 35px;
  height: 35px;
  background: transparent;
  border-radius: 60px;
  border: 1px solid #fff;
  cursor: pointer;
}
.baselinemenu img {
  width: 21px;
  height: 21px;
}

.main-menu-small {
  display: none;
}

@media (max-width: 900px) {
  .main-menu {
    display: none;
  }
  .main-menu-content-small {
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .main-menu-small {
    display: block;
    padding: 40px 0;
  }
}
</style>
