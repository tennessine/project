<template>
  <div class="hello">
    <div class="addresses">
      <div class="address" v-for="(address, index) in addressList" :key="index" :class="{ active: address.isDefault }">
        <div class="info">
          <div class="contact">
            <span class="name">收货人: 葛孔飞</span>
            <span class="phone">13632613407</span>
          </div>
          <div class="detail">
            北京北京市昌平区于辛庄村迦美家园2栋104
          </div>
        </div>
        <div class="default">
          <span v-if="address.isDefault">√</span>
        </div>
      </div>
    </div>
    <a class="add">新增收货地址</a>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      addressList: [{
        name: '葛孔飞',
        phone: '13632613407',
        address: ' 北京北京市昌平区于辛庄村迦美家园2栋104',
        isDefault: true
      }, {
        name: '葛孔飞',
        phone: '13632613407',
        address: ' 北京北京市昌平区于辛庄村迦美家园2栋104',
        isDefault: false
      }, {
        name: '葛孔飞',
        phone: '13632613407',
        address: ' 北京北京市昌平区于辛庄村迦美家园2栋104',
        isDefault: false
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
  .addresses {
    background: rgb(238, 238, 238);
    .address {
      display: flex;
      align-items: center;
      color: #222;
      background: #fff;
      margin-top: 20px;
      .info {
        flex: 1;
        display: flex;
        flex-direction: column;
        padding: 20px;
        .contact {
          font-size: 30px;
          display: flex;
          .phone {
            flex: 1;
            display: flex;
            justify-content: flex-end;
          }
        }
        .detail {
          font-size: 30px;
          margin-top: 20px;
        }
      }
      .default {
        width: 60px;
      }
    }
    .active {
      background: rgb(94, 107, 133);
      color: #fff;
    }
  }
  .add {
    background: rgb(255, 85, 0);
    color: #fff;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    font-size: 30px;
    height: 80px;
    line-height: 80px;
    text-align: center;
  }
</style>
