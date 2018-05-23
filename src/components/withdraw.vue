<template>
  <div class="withdraw">
    <div class="wallet">
      提现到：微信钱包
    </div>
    <p class="info">
      微信支付将收取0.6手续费，24小时内到账
    </p>
    <div class="amount">
      <h2>提现金额</h2>
      <div class="input-box">
        <span class="unit">¥</span>
        <input type="number" class="input" placeholder="请输入金额" />
      </div>
    </div>
    <div class="available">
      可提现金额 ¥0.00, <a>全部提现</a>
    </div>
    <div class="tip">
      每月可提现5次，当前剩余5次
    </div>
    <div class="action">
      <a href="">申请提现</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .withdraw {
    font-size: 30px;
    width: 80%;
    margin: 40px auto 0;
    .wallet {
      color: rgb(92, 95, 112);
      font-weight: 700;
    }
    .info {
      color: rgb(161, 161, 161);
      margin-top: 20px;
    }
    .amount {
      h2 {
        font-size: 30px;
      }
      .input-box {
        .unit {
          font-size: 60px;
        }
        .input {
          font-size: 30px;
          border: none;
          outline: none;
          background: transparent;
          margin-left: 20px;
        }
      }
    }
    .available {
      color: rgb(158, 158, 158);
      margin-top: 60px;
      a {
        color: rgb(254, 46, 82);
      }
    }
    .tip {
      color: rgb(158, 158, 158);
      margin-top: 10px;
    }
    .action {
      margin-top: 40px;
      a {
        display: inline-block;
        text-decoration: none;
        color: #fff;
        background: rgb(254, 46, 82);
        width: 500px;
        height: 80px;
        line-height: 80px;
        text-align: center;
        border-radius: 10px;
      }
    }
  }
</style>
