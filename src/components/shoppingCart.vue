<template>
  <div class="shopping-cart">
    <div class="cart-info">
      <div class="cart-item">
        <div class="header">
          <input class="check" type="radio" />
          <img class="shop-icon" src="@/assets/shop.svg" alt="" />
          <span class="name">CandyDream糖果梦 <img class="more" src="@/assets/more.svg" alt="" /></span>
          <span class="edit">编辑</span>
        </div>
        <div class="product">
          <input class="check" type="radio" />
          <img class="product-img" src="https://gw.alicdn.com/bao/uploaded/i3/695277835/TB26uEomQOWBuNjSsppXXXPgpXa_!!695277835.jpg_200x200q50s150.jpg_.webp" alt="">
          <div class="product-info">
            <div class="product-name">宠物猫咪产房怀孕猫产房产箱折叠户外帐篷狗狗封闭式窝猫生产用品</div>
            <div class="product-detail">
              <div class="product-price">
                <span class="shop-price">¥99.00</span>
                <span class="market-price">¥198.00</span>
              </div>
              <div class="amount">
                ×9
              </div>
            </div>
          </div>
        </div>
        <div class="product">
          <input class="check" type="radio" />
          <img class="product-img" src="https://gw.alicdn.com/bao/uploaded/i3/695277835/TB26uEomQOWBuNjSsppXXXPgpXa_!!695277835.jpg_200x200q50s150.jpg_.webp" alt="">
          <div class="product-info">
            <div class="product-name">宠物猫咪产房怀孕猫产房产箱折叠户外帐篷狗狗封闭式窝猫生产用品</div>
            <div class="product-detail">
              <div class="product-price">
                <span class="shop-price">¥99.00</span>
                <span class="market-price">¥198.00</span>
              </div>
              <div class="amount">
                ×1
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="cart-item">
        <div class="header">
          <input class="check" type="radio" />
          <img class="shop-icon" src="@/assets/shop.svg" alt="" />
          <span class="name">CandyDream糖果梦 <img class="more" src="@/assets/more.svg" alt="" /></span>
          <span class="edit">编辑</span>
        </div>
        <div class="product">
          <input class="check" type="radio" />
          <img class="product-img" src="https://gw.alicdn.com/bao/uploaded/i3/2831155458/TB28YGIfyCYBuNkHFCcXXcHtVXa_!!2831155458.jpg_200x200q50s150.jpg_.webp" alt="">
          <div class="product-info">
            <div class="product-name">宠物猫咪产房怀孕猫产房产箱折叠户外帐篷狗狗封闭式窝猫生产用品</div>
            <div class="product-detail">
              <div class="product-price">
                <span class="shop-price">¥99.00</span>
                <span class="market-price">¥198.00</span>
              </div>
              <div class="amount">
                ×2
              </div>
            </div>
          </div>
        </div>
        <div class="product">
          <input class="check" type="radio" />
          <img class="product-img" src="https://gw.alicdn.com/bao/uploaded/i4/627243310/TB2O0_.hAKWBuNjy1zjXXcOypXa_!!627243310.jpg_200x200q50s150.jpg_.webp" alt="">
          <div class="product-info">
            <div class="product-name">宠物猫咪产房怀孕猫产房产箱折叠户外帐篷狗狗封闭式窝猫生产用品</div>
            <div class="product-detail">
              <div class="product-price">
                <span class="shop-price">¥99.00</span>
                <span class="market-price">¥198.00</span>
              </div>
              <div class="amount">
                ×3
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="total-info">
      <div class="left">
        <label>
          <input class="check" type="radio" />
          全选
        </label>
        <span class="total">合计: ¥0.00</span>
      </div>
      <a class="right">结算(0)</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .shopping-cart {
    background: rgb(238, 238, 238);
    .cart-info {
      .cart-item {
        .header {
          display: flex;
          align-items: center;
          height: 80px;
          background: #fff;
          .check {
            width: 80px;
          }
          .shop-icon {
            width: 30px;
            height: 30px;
          }
          .name {
            margin-left: 10px;
            font-size: 24px;
            display: flex;
            align-items: center;
            flex: 1;
            .more {
              margin-left: 20px;
              width: 30px;
              height: 30px;
            }
          }
          .edit {
            font-size: 24px;
            padding-right: 30px;
          }
        }
        .product {
          display: flex;
          align-items: center;
          padding: 20px;
          background: rgb(245, 245, 245);
          .check {
            width: 80px;
          }
          .product-img {
            width: 160px;
            height: 160px;
          }
          .product-info {
            padding: 20px 10px 20px;
            .product-name {
              font-size: 30px;
            }
            .product-detail {
              display: flex;
              padding-top: 30px;
              .product-price {
                font-size: 30px;
                flex: 1;
                .shop-price {
                  color: #f60;
                }
                .market-price {
                  text-decoration: line-through;
                  color: #999;
                  font-size: 24px;
                }
              }
              .amount {
                font-size: 30px;
              }
            }
          }
        }
      }
    }
    .total-info {
      position: fixed;
      left: 0;
      right: 0;
      bottom: 0;
      background: #fff;
      font-size: 30px;
      display: flex;
      height: 80px;
      align-items: center;
      .left {
        flex: 3;
        display: flex;
        padding: 0 20px;
        label {
          flex: 1;
          .check {
            margin-right: 10px;
          }
        }
      }
      .right {
        flex: 1;
        color: #fff;
        background: rgb(255, 85, 0);
        line-height: 80px;
        text-align: center;
      }
    }
  }
</style>
