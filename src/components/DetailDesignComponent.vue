<template>
  <div class="main-container">
    <img class="main-container-down" src="@/assets/images/detail.svg" />
    <img class="main-container-upper" src="@/assets/images/detailarrow.svg" />
  </div>
  <div class="main-container-small">
    <img class="main-container-down" src="@/assets/images/detail2.svg" />
    <img class="main-container-upper" src="@/assets/images/detailarrow2.svg" />
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  justify-content: center;

  background: url('@/assets/images/header-background.svg');
  background-repeat: no-repeat;
  background-size: 120%;
  background-position: center bottom;
}
.main-container-down {
  position: relative;
  z-index: 0;
}
.main-container-upper {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.main-container-small {
  display: none;
}

@media (max-width: 1085px) {
  .main-container {
    display: none;
  }
  .main-container-small {
    display: block;
    display: flex;
    justify-content: center;
    z-index: -10;

    background: url('@/assets/images/header-background.svg');
    background-repeat: no-repeat;
    background-size: 120%;
    background-position: center bottom;
  }
}
</style>
