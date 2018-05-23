<template>
  <div class="hello">
    <div class="bottom">
      <div class="left">
        <div class="shop item">
          <img src="@/assets/shop.svg" alt="">
          <span>店铺</span>
        </div>
        <div class="contact item">
          <img src="@/assets/contact.svg" alt="">
          <span>客服</span>
        </div>
        <div class="favorite item">
          <img src="@/assets/favorite.svg" alt="">
          <span>收藏</span>
        </div>
      </div>
      <div class="right">
        <a class="cart">加入购物车</a>
        <a class="buy">立即购买</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Bottom'
}
</script>

<style lang="scss" scoped>
  .bottom {
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    height: 80px;
    .left {
      flex: 1;
      font-size: 30px;
      display: flex;
      justify-content: center;
      align-items: center;
      .item {
        flex: 1;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        img {
          width: 40px;
          height: 40px;
        }
        span {
          margin-top: 10px;
          font-size: 24px;
        }
      }
    }
    .right {
      flex: 1;
      display: flex;
      a {
        flex: 1;
        display: flex;
        font-size: 30px;
        color: #fff;
        align-items: center;
        justify-content: center;
      }
      .cart {
        background: rgb(255, 149, 0);
      }
      .buy {
        background: rgb(255, 0, 54);
      }
    }
  }
</style>
