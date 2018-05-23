<template>
  <div class="order">
    <div class="address">
      <img class="location" src="@/assets/location.svg" alt="">
      <div class="address-info">
        <div class="contact">
          <span class="name">收货人：葛孔飞</span>
          <span class="phone">13632613407</span>
        </div>
        <div class="detail">
          收货地址：北京 北京市 昌平区 沙河镇 沙河 于辛庄村迦美家园2栋014
        </div>
      </div>
      <img class="more" src="@/assets/more.svg" alt="">
    </div>
    <div class="product">
      <h1 class="shop-info">
        <img class="logo" src="https://img.alicdn.com/tps/i2/TB1wopUHVXXXXXyXpXXAAT2HVXX-63-63.png" alt="">
        满意百分百商城
      </h1>
      <div class="product-info">
        <img class="product-img" src="https://gw.alicdn.com/bao/uploaded/i2/248398811/TB2DLpkXdqUQKJjSZFIXXcOkFXa_!!248398811.jpg_270x270q90.jpg" alt="">
        <div class="product-detail">
          <div class="product-name">
            帆布鞋男2018春季新款系带平底运动休闲布鞋男士低帮潮流百搭板鞋
          </div>
          <div class="product-price">
            ¥89.00
          </div>
        </div>
        <div class="amount">
          ×2
        </div>
      </div>
    </div>
    <div class="item">
      <span class="label">购买数量</span>
      <span class="content">
        <number-box></number-box>
      </span>
    </div>
    <div class="item">
      <span class="label">给卖家留言:</span>
      <span class="content">
        <input type="text" placeholder="选填: 填写内容已和卖家协商确认" />
      </span>
    </div>
    <div class="stat">
      共1件，合计：<span class="price">¥89.00</span>
    </div>
    <div class="bottom-bar">
      <div class="total">
        共<span class="amount">1</span>件，
        总金额<span class="price">¥ 89.00</span>
      </div>
      <a class="btn">提交订单</a>
    </div>
  </div>
</template>

<script>
import NumberBox from '@/components/NumberBox.vue'
export default {
  components: {
    NumberBox
  }
}
</script>

<style lang="scss" scoped>
  .order {
    background: rgb(238, 238, 238);
    .address {
      display: flex;
      align-items: center;
      padding: 30px 20px;
      border-bottom: 1px solid #ddd;
      background: #fff;
      .location {
        width: 30px;
        height: 30px;
      }
      .address-info {
        font-size: 28px;
        padding: 0 10px;
        .contact {
          display: flex;
          .phone {
            flex: 1;
            text-align: right;
          }
        }
        .detail {
          margin-top: 20px;
          line-height: 40px;
        }
      }
      .more {
        width: 30px;
        height: 30px;
      }
    }
    .product {
      background: #fff;
      .shop-info {
        font-size: 26px;
        display: flex;
        align-items: center;
        padding: 10px 20px;
        font-weight: normal;
        .logo {
          width: 40px;
          height: 40px;
          margin-right: 20px;
        }
      }
      .product-info {
        display: flex;
        align-items: center;
        padding-left: 20px;
        .product-img {
          width: 140px;
          height: 140px;
        }
        .product-detail {
          flex: 1;
          padding: 0 20px;
          .product-name {
            font-size: 28px;
            color: #666;
            line-height: 40px;
          }
          .product-price {
            font-size: 30px;
            margin-top: 10px;
            color: #f50;
            font-weight: bold;
          }
        }
        .amount {
          width: 60px;
          font-size: 30px;
          color: #666;
        }
      }
    }
    .item {
      display: flex;
      align-items: center;
      padding: 30px 20px;
      border-bottom: 1px solid #ddd;
      background: #fff;
      .label {
        font-size: 26px;
        color: #666;
        width: 200px;
        display: inline-block;
      }
      .content {
        flex: 1;
        display: flex;
        align-items: center;
        input {
          border: none;
          background: transparent;
          font-size: 26px;
          width: 500px;
          outline: none;
        }
      }
    }
    .stat {
      background: #fff;
      font-size: 26px;
      font-weight: 700;
      text-align: right;
      height: 80px;
      line-height: 80px;
      padding-right: 20px;
      border-bottom: 1px solid #bbb;
      .price {
        color: #f50;
      }
    }
    .bottom-bar {
      border-top: 1px solid #bbb;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 80px;
      display: flex;
      align-items: center;
      .total {
        font-size: 30px;
        flex: 1;
        text-align: right;
        padding-right: 20px;
        .price {
          color: #f50;
          font-weight: 700;
        }
        .amount {
          color: #f50;
        }
      }
      .btn {
        display: inline-block;
        width: 200px;
        line-height: 80px;
        background: #f50;
        color: #fff;
        font-size: 30px;
        text-align: center;
      }
    }
  }
</style>
