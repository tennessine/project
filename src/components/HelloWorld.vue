<template>
  <div class="company">
    <div class="tab-btns">
      <div
        v-for="(tab, index) in tabs"
        :key="index"
        class="tab-btn"
        :class="{ active: index === currentIndex }"
        @click="selectTab(index)">
        <span>{{ tab }}</span>
      </div>
    </div>
    <div class="tab-contents">
      <div class="tab-content" v-if="currentIndex === 0">
        <div class="basic-info">
          <dl>
            <dt>公司名称</dt>
            <dd>台州德涛机电有限公司</dd>
          </dl>
          <dl>
            <dt>经营模式</dt>
            <dd>生产厂家</dd>
          </dl>
          <dl>
            <dt>所在地区</dt>
            <dd>浙江 温岭市</dd>
          </dl>
          <dl>
            <dt>主营产品</dt>
            <dd>自吸泵、螺杆泵、潜水泵、深井泵、增压泵</dd>
          </dl>
          <dl>
            <dt>商品数量</dt>
            <dd>70条</dd>
          </dl>
        </div>
        <div class="contact-info">
          <dl>
            <dt>联系人</dt>
            <dd>王乃月</dd>
          </dl>
          <dl>
            <dt>联系电话</dt>
            <dd>136 3261 3407</dd>
          </dl>
          <dl>
            <dt>联系地址</dt>
            <dd>浙江温岭市大溪镇良山工业区</dd>
          </dl>
        </div>
        <div class="company-location">
          <el-amap vid="amapDemo" :plugin="plugin" :center="center" :map-manager="amapManager" :zoom="zoom" class="amap">
          </el-amap>
        </div>
      </div>
      <div class="tab-content" v-else>
        <div class="authenticate">
          <div class="integrity">诚信通 <span>4</span> 年</div>
          <div class="auth">通过第三方深度验厂</div>
        </div>
        <div class="company-pictures">
          <h4>企业实力认证信息</h4>
          <div class="albums">
            <div class="album">
              <img src="https://img.alicdn.com/i2/0/TB2kYP3f9YH8KJjSspdXXcRgVXa_!!0-av-auth-doc.jpg" alt="">
              <p>厂房外景(1)</p>
            </div>
            <div class="album">
              <img src="https://img.alicdn.com/i2/0/TB2l37VfZLJ8KJjy0FnXXcFDpXa_!!0-av-auth-doc.jpg" alt="">
              <p>办公场所(1)</p>
            </div>
            <div class="album">
              <img src="https://img.alicdn.com/i2/0/TB2y6K6bjgy_uJjSZJnXXbuOXXa_!!0-av-auth-doc.jpg" alt="">
              <p>常规设备(4)</p>
            </div>
            <div class="album">
              <img src="https://img.alicdn.com/i4/0/TB2Km3nf8TH8KJjy0FiXXcRsXXa_!!0-av-auth-doc.jpg" alt="">
              <p>营业执照(1)</p>
            </div>
          </div>
        </div>
        <div class="company-ability">
          <h4>企业能力标签</h4>
          <div class="labels">
            <span class="label">原厂工厂</span>
            <span class="label">自有品牌</span>
            <span class="label">OEM代工</span>
            <span class="label">ODM代工</span>
            <span class="label">OBM代工</span>
          </div>
        </div>
        <div class="business-info">
          <h4>工商注册信息</h4>
          <dl>
            <dt>公司名称</dt>
            <dd>台州德涛机电有限公司</dd>
          </dl>
          <dl>
            <dt>经营地址</dt>
            <dd>中国浙江台州温岭市大溪镇岗上村2区72号</dd>
          </dl>
          <dl>
            <dt>成立日期</dt>
            <dd>2011年12月12日</dd>
          </dl>
          <dl>
            <dt>经营范围</dt>
            <dd>电机、水泵、振动器、电焊机、空压机、切割机、风机、电动工具制造、加工、销售；货物进出口、技术进出口。</dd>
          </dl>
          <dl>
            <dt>注册号</dt>
            <dd>91331081587779307F</dd>
          </dl>
          <dl>
            <dt>法人代表</dt>
            <dd>金妙鲜</dd>
          </dl>
          <dl>
            <dt>企业类型</dt>
            <dd>私营有限责任公司</dd>
          </dl>
          <dl>
            <dt>营业期限</dt>
            <dd>2011-12-12 至 2031-12-11</dd>
          </dl>
          <dl>
            <dt>登记机关</dt>
            <dd>温岭市市场监督管理局</dd>
          </dl>
        </div>
      </div>
    </div>
    <div class="bottom-bar">
      <div class="btn wechat">微信号</div>
      <div class="btn phone">拨打电话</div>
    </div>
  </div>
</template>

<script>
import { AMapManager } from 'vue-amap'
let amapManager = new AMapManager()
export default {
  data: function () {
    return {
      tabs: ['基本信息', '认证信息'],
      currentIndex: 0,
      zoom: 12,
      center: [121.59996, 31.197646],
      amapManager,
      plugin: [{
        pName: 'ToolBar',
        events: {
          init (instance) {
            console.log(instance)
          }
        }
      }]
    }
  },
  methods: {
    selectTab (index) {
      this.currentIndex = index
    }
  }
}
</script>

<style lang="scss" scoped>
  .company {
    background: rgb(245, 245, 245);
    .tab-btns {
      background: #fff;
      display: flex;
      border-bottom: 1px solid #d5d5d5; /*no*/
      .tab-btn {
        flex: 1;
        text-align: center;
        font-size: 30px;
        span {
          display: inline-block;
          width: 190px;
          height: 80px;
          line-height: 80px;
        }
        &.active {
          span {
            color: #FF7300;
            border-bottom: 2px solid #FF7300; /*no*/
          }
        }
      }
    }
    .tab-contents {
      margin-top: 10px;
      margin-bottom: 100px;
      .tab-content {
        dl {
          border-bottom: 1px solid #eee; /*no*/
          font-size: 26px;
          margin: 0;
          display: flex;
          padding: 15px 0;
          align-items: center;
          padding-left: 14px;
          dt {
            width: 140px;
            &::after {
              content: "：";
            }
          }
          dd {
            flex: 1;
            margin: 0;
          }
        }
        .basic-info, .contact-info {
          background: #fff;
        }
        .contact-info {
          margin-top: 10px;
        }
        .company-location {
          margin-top: 10px;
          .amap {
            height: 500px;
          }
        }
        .authenticate {
          background: #fff;
          font-size: 26px;
          .integrity {
            background: url("../assets/integrity.png") no-repeat 20px center;
            background-size: 20px 20px; /*no*/
            padding-left: 60px;
            line-height: 60px;
            padding-left: 70px;
            border-bottom: 1px solid #eee;
          }
          .auth {
            background: url("../assets/authenticate.png") no-repeat 20px center;
            background-size: 20px 20px; /*no*/
            padding-left: 60px;
            line-height: 60px;
            padding-left: 70px;
            border-bottom: 1px solid #ddd;
          }
        }
        .company-pictures {
          h4 {
            margin: 20px 0;
            padding-left: 20px;
            font-size: 20px;
            color: #B1B1B1;
          }
          .albums {
            display: flex;
            background: #fff;
            padding: 20px;
            .album {
              margin-right: 10px;
              img {
                width: 140px;
                height: 140px;
              }
              p {
                font-size: 20px;
                margin: 0;
                text-align: center;
              }
            }
          }
        }
        .company-ability {
          h4 {
            margin: 20px 0;
            padding-left: 20px;
            font-size: 20px;
            color: #B1B1B1;
          }
          .labels {
            display: flex;
            flex-wrap: wrap;
            background: #fff;
            padding: 10px 0;
            .label {
              border: 1px solid #ff2000; /*no*/
              color: #ff2000;
              width: 158px;
              height: 40px;
              margin: 10px 20px 10px 20px;
              line-height: 40px;
              text-align: center;
              font-size: 24px;
            }
          }
        }
        .business-info {
          h4 {
            margin: 20px 0;
            padding-left: 20px;
            font-size: 20px;
            color: #B1B1B1;
          }
          dl {
            background: #fff;
            padding-left: 20px;
          }
        }
      }
    }
    .bottom-bar {
      display: flex;
      position: fixed;
      left: 0;
      right: 0;
      bottom: 0;
      .btn {
        flex: 1;
        height: 80px;
        line-height: 80px;
        font-size: 30px;
        text-align: center;
      }
      .wechat {
        background: #FDE9D6;
        color: #F67300;
      }
      .phone {
        background: #F67300;
        color: #FFF;
      }
    }
  }
</style>
