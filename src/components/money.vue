<template>
  <div class="user-balance">
    <div class="user-money">
      <div class="money">¥0.00</div>
      <div class="description">账户余额</div>
    </div>
    <div class="user-action">
      <a class="btn withdraw">提现</a>
      <a class="btn recharge" @click="prepareRecharge">充值</a>
    </div>
    <transition name="slide">
      <div class="cover" v-if="showRechargeModal" @click="closeRechargeModal">
        <div class="recharge-modal">
          <h2>充值金额</h2>
          <div class="amount">
            <span :class="{ active: amount === currentAmount }" v-for="amount in selectableAmount" :key="amount" @click.stop="setAmount(amount)">{{ amount }}元</span>
          </div>
          <input class="input" type="text" placeholder="请输入其他金额" v-model="currentAmount" @click.stop="_ => {}" />
          <a class="btn" @click.stop="confirmRecharge">确定</a>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      showRechargeModal: false,
      currentAmount: 50,
      selectableAmount: [50, 100, 200]
    }
  },
  methods: {
    prepareRecharge () {
      this.showRechargeModal = true
    },
    closeRechargeModal () {
      this.showRechargeModal = false
    },
    confirmRecharge () {
      this.showRechargeModal = false
    },
    setAmount (amount) {
      this.currentAmount = amount
    }
  }
}
</script>

<style lang="scss" scoped>
  .slide-enter, .slide-leave-to {
    transform: translateY(-100%);
  }
  .user-balance {
    .user-money {
      background: rgb(255, 45, 81);
      color: #fff;
      display: flex;
      align-items: center;
      flex-direction: column;
      justify-content: center;
      .money {
        font-size: 80px;
        margin-top: 40px;
      }
      .description {
        font-size: 30px;
        padding: 20px 0;
      }
    }
    .user-action {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      display: flex;
      padding: 30px 20px;
      .btn {
        flex: 1;
        font-size: 40px;
        padding: 20px;
        text-align: center;
        border-radius: 10px;
      }
      .withdraw {
        background: #ddd;
        color: #222;
      }
      .recharge {
        background: rgb(255, 45, 81);
        margin-left: 20px;
        color: #fff;
      }
    }
    .cover {
      position: fixed;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      background: rgba(0, 0, 0, .2);
      z-index: 999;
      transition: all .3s;
      .recharge-modal {
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        background: #fff;
        color: #333;
        display: flex;
        flex-direction: column;
        font-size: 30px;
        padding: 30px 20px;
        h2 {
          text-align: center;
          font-weight: normal;
          font-size: 30px;
        }
        .amount {
          display: flex;
          .active {
            background: rgb(255,45,81);
            color: #fff;
          }
          span {
            flex: 1;
            text-align: center;
            padding: 10px 0;
          }
        }
        .input {
          font-size: 30px;
          margin-top: 30px;
          border: none;
          outline: none;
          background: transparent;
        }
        .btn {
          display: inline-block;
          width: 90%;
          margin: 40px auto;
          padding: 20px;
          background: rgb(255,45,81);
          border-radius: 10px;
          color: #fff;
          text-align: center;
        }
      }
    }
  }
</style>

