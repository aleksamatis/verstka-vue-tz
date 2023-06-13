<template>
  <div class="root">
    <div class="clients-main-container">
      <div class="box">
        <div>
          <img src="@/assets/images/clients.svg" alt="" />
        </div>
        <div class="team-members-item">
          <div><img src="@/assets/images/client1.jpg" alt="" /></div>
          <div>Белякинов</div>
          <div>Ярослав</div>
          <div class="item-description">Евроремонт</div>
        </div>
        <div class="team-members-item">
          <div><img src="@/assets/images/client2.jpg" alt="" /></div>
          <div>Сорокина</div>
          <div>Ольга</div>
          <div class="item-description">Евроремонт</div>
        </div>
        <div class="team-members-item">
          <div><img src="@/assets/images/client3.jpg" alt="" /></div>
          <div>Самсонов</div>
          <div>Кирилл</div>
          <div class="item-description">Евроремонт</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.clients-main-container {
  display: flex;
}

.box {
  display: flex;
  min-height: min-content;
  justify-content: space-between;
  flex: 1;
}

.team-members-item {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(7.5px);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #fff;
  padding: 20px;
  text-align: center;
  font-size: 10px;
  width: 130px;
  height: 150px;
}

.team-members-item .item-description {
  color: rgba(255, 255, 255, 0.7);
}

.team-members-item img {
  border-radius: 100%;
}

@media screen and (max-width: 900px) {
  .box {
    width: 0;
  }
  .clients-main-container {
    position: relative;
    overflow: auto;
    margin-left: -83px;
    margin-right: -83px;
    padding-left: 83px;
  }

  .root {
    position: relative;
  }

  .root::before {
    content: ' ';
    position: absolute;
    background: rgba(23, 35, 54, 0.76);
    filter: blur(13px);
    width: 83px;
    top: 0;
    left: -83px;
    height: 100%;
    z-index: 3;
  }

  .root::after {
    content: ' ';
    position: absolute;
    background: rgba(23, 35, 54, 0.76);
    filter: blur(13px);
    width: 83px;
    top: 0;
    right: -83px;
    height: 100%;
  }

  .clients-main-container .box > * {
    margin-right: 15px;
  }
}
</style>
