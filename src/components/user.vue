<template>
  <div class="user">
    <div class="user-info">
      <div class="user-wrapper">
        <div class="user-setting">
          <img src="@/assets/gear.svg" alt="">
          <img src="@/assets/rocket.svg" alt="">
        </div>
        <div class="user-avatar">
          <img class="avatar" src="http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/132?t=1526982272" alt="">
          <div class="info">
            <div class="user-nickname">
              爱吃猫粮的鱼
            </div>
            <div class="user-gender">
              <img src="@/assets/female.svg" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="user-container">
      <div class="score">
        <div class="user-money">
          <div class="balance">¥ 0.00</div>
          <div class="description">钱包</div>
        </div>
        <div class="user-point">
          <div class="point">0</div>
          <div class="description">积分</div>
        </div>
      </div>
      <div class="nav">
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
        <div class="link">
          <span>我的幸福圈</span>
          <img src="@/assets/more.svg" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .user {
    .user-info {
      background: url("https://assets.qingmei.me/v2/app/user/img/bg1.jpg") no-repeat;
      background-size: cover;
      width: 750px;
      height: 400px;
      .user-wrapper {
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, .2);
        position: relative;
        .user-setting {
          position: absolute;
          right: 0;
          top: 0;
          display: flex;
          flex-direction: column;
          width: 60px;
          img {
            margin-top: 30px;
            width: 40px;
            height: 40px;
          }
        }
        .user-avatar {
          display: flex;
          flex-direction: column;
          align-items: center;
          padding-top: 100px;
          .avatar {
            width: 137px;
            height: 137px;
            border: 4px solid rgba(255, 255, 255, .5);
            border-radius: 50%;
          }
          .info {
            margin-top: 20px;
            display: flex;
            align-items: center;
            .user-nickname {
              font-size: 30px;
              color: #fff;
              font-weight: bold;
            }
            .user-gender {
              margin-left: 10px;
              background: #4ebdf9;
              width: 40px;
              height: 40px;
              border-radius: 50%;
              display: flex;
              align-items: center;
              justify-content: center;
              img {
                width: 30px;
                height: 30px;
              }
            }
          }
        }
      }
    }
    .user-container {
      padding: 30px 40px;
      .score {
        display: flex;
        .user-money {
          flex: 1;
          .balance {
            color: rgb(255, 45, 81);
            font-size: 48px;
            font-weight: 700;
          }
          .description {
            font-size: 24px;
            color: #999;
            margin-top: 10px;
          }
        }
        .user-point {
          flex: 1;
          .point {
            font-size: 48px;
            color: #333;
          }
          .description {
            font-size: 24px;
            color: #999;
            margin-top: 10px;
          }
        }
      }
      .nav {
        margin-top: 80px;
        display: flex;
        flex-wrap: wrap;
        .link {
          display: flex;
          align-items: center;
          width: 50%;
          height: 80px;
          span {
            color: #535353;
            font-size: 30px;
            flex: 1;
          }
          img {
            width: 30px;
            height: 30px;
            margin-right: 20px;
          }
        }
      }
    }
  }
</style>

