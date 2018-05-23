<template>
  <div class="address">
    <div class="form">
      <div class="item">
        <div class="left">
          北京北京市东城区
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
      <div class="item">
        <div class="left">
          北新桥街道
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
      <div class="item">
        <div class="left">
          <input type="text" placeholder="请输入详细地址" />
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
      <div class="item">
        <div class="left">
          <input type="text" placeholder="请输入收货人姓名" />
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
      <div class="item">
        <div class="left">
          <input type="text" placeholder="请输入收货人联系电话" />
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
      <div class="item">
        <div class="left">
          <input type="text" placeholder="10010" />
        </div>
        <div class="right">
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
    </div>
    <div class="save">
      <a href="">保存地址</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .address {
    background: rgb(238, 238, 238);
    .form {
      .item {
        display: flex;
        align-items: center;
        border-bottom: 1px solid rgb(221, 221, 221);
        padding: 20px 30px;
        .left {
          flex: 1;
          font-size: 30px;
          input {
            width: 100%;
            border: none;
            background: transparent;
            outline: none;
          }
        }
        .right {
          img {
            width: 40px;
            height: 40px;
          }
        }
      }
    }
    .save {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      a {
        display: block;
        background: rgb(255, 85, 0);
        color: #fff;
        text-decoration: none;
        font-size: 30px;
        text-align: center;
        line-height: 80px;
      }
    }
  }
</style>

