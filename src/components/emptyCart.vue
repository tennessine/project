<template>
  <div class="empty">
    <div class="img-wrapper">
      <img src="@/assets/images/cart.png" alt="">
    </div>
    <div class="title">购物车快饿扁了T.T</div>
    <div class="sub">主人快给我挑点宝贝吧</div>
    <a class="find">去逛逛</a>
  </div>
</template>

<style lang="scss" scoped>
  .empty {
    background: rgb(238, 238, 238);
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100%;
    .img-wrapper {
      width: 238px;
      height: 238px;
      background: #ccc;
      border-radius: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 213px;
      img {
        width: 140px;
        height: 140px;
      }
    }
    .title {
      font-size: 28px;
      margin-top: 20px;
    }
    .sub {
      color: #999;
      font-size: 24px;
      margin-top: 20px;
    }
    .find {
      font-size: 30px;
      border: 1px solid #051b28;
      border-radius: 10px;
      padding: 10px 60px;
      margin-top: 20px;
    }
  }
</style>

