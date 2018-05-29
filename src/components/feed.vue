<template>
  <div class="business-record">
    <div class="record" v-for="(record, index) in records" :key="index">
      <div class="user-info">
        <img class="avatar" :src="record.userInfo.avatar" alt="">
        <span class="nickname">{{ record.userInfo.nickname }}</span>
        <span class="gender">
          <img src="@/assets/male.svg" alt="">
        </span>
      </div>
      <div class="content">
        {{ record.content }}
      </div>
      <div class="imgs">
        <div class="img-wrapper" v-for="(img, index) in record.imgs" :key="index">
          <img :src="img" alt="">
        </div>
      </div>
      <div class="panel">
        <span class="publish-at">9分钟前</span>
        <img @click="leaveComment(record)" class="leave-comment" src="@/assets/comment.svg" alt="">
        <div class="toolbar" v-if="record.showToolbar">
          <span class="like">赞 <img src="@/assets/heart.svg" alt=""></span>
          <span class="review">评论 <img src="@/assets/review.svg" alt=""></span>
        </div>
      </div>
      <div class="comments">
        <div class="upvote">
          <span class="count">{{ record.votes.count }}赞</span>
          <div class="avatar-list">
            <img class="avatar" v-for="(avatar, index) in record.votes.avatarList" :key="index" :src="avatar" alt="">
          </div>
        </div>
        <div class="comment" v-for="(comment, index) in record.comments" :key="index">
          <span class="nickname">{{ comment.nickname }}: </span> {{ comment.content }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      records: [{
        userInfo: {
          avatar: 'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
          nickname: '爱吃猫粮的鱼',
          gender: 1
        },
        content: '上学那会的男神无非就是学习好的或者是打球最帅的，根本没有现在所谓的高富帅。',
        imgs: [
          'http://static.qingmei.me/20180529/d557d61620601bd34d36a5ddbbf9364e.jpg/640?sign=5818531c39d5e1d489ff1077d008cfb1&t=5b102a10',
          'http://static.qingmei.me/20180529/0307aed07e27bc44001a37c347459d3d.jpg/200?sign=1bb44e70fe4ad263efc1f78ccf247b3b&t=5b102a10'
        ],
        publishAt: '2018-05-29 10:00:00',
        votes: {
          count: 1,
          avatarList: [
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272'
          ]
        },
        comments: [{
          nickname: '爱吃猫粮的鱼',
          content: '谢谢'
        }, {
          nickname: '爱吃猫粮的鱼',
          content: `前几天街上走着，突然一个很漂亮的小姐姐拿着一个手机问我，小哥哥，小哥哥，你看我的手机是不是有什么问题？好像缺点儿什么？我一看是水果最新款，解屏没什么问题，我说，没问题啊？功能很全什么也不缺～这时小姐姐迷之微笑的说，缺你的微信啊？我去居然这么漂亮的小姐姐套路我？我愉快的加了她的微信……结果这几天我才发现，这货是微商……`
        }],
        showToolbar: false
      }, {
        userInfo: {
          avatar: 'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
          nickname: '爱吃猫粮的鱼',
          gender: 0
        },
        content: `上学那会的男神无非就是学习好的或者是打球最帅的，根本没有现在所谓的高富帅。我的男神就不一样了，他是我们生物实验小组第一个解 剖青蛙的！当时觉得，就这手法，在古代一定是个征战沙场的将军！后来发现，他家是卖烧烤的……`,
        imgs: [
          'http://static.qingmei.me/20180529/d557d61620601bd34d36a5ddbbf9364e.jpg/640?sign=5818531c39d5e1d489ff1077d008cfb1&t=5b102a10',
          'http://static.qingmei.me/20180529/0307aed07e27bc44001a37c347459d3d.jpg/200?sign=1bb44e70fe4ad263efc1f78ccf247b3b&t=5b102a10',
          'http://static.qingmei.me/20180529/03b65dd11d3e6662345e2ca33cd0e1d4.jpg/200?sign=868feba4c5453b90610b224efedb0ce5&t=5b102a10',
          'http://static.qingmei.me/20180529/cce2207ebaa75af2be2d18aa1d5ed46e.jpg/200?sign=d89b99f8d39023792573df825f798c9c&t=5b102a10',
          'http://static.qingmei.me/20180529/cce2207ebaa75af2be2d18aa1d5ed46e.jpg/200?sign=d89b99f8d39023792573df825f798c9c&t=5b102a10',
          'http://static.qingmei.me/20180529/5d51e83813116e60819f1abab9c3a581.jpg/200?sign=e3ffeb18584e2b93f58227dd4f0636c9&t=5b102a10',
          'http://static.qingmei.me/20180529/d7e57f6ca2be228ea78a5be1139fd2a1.jpg/200?sign=6fa386e931d0c0c4bbdbf00b4dfd4629&t=5b102a10',
          'http://static.qingmei.me/20180529/d568c79d9319b623bfe13c0d6a9e0cc9.jpg/200?sign=8bbf012b095cf35b17f76906e14d133f&t=5b102a10',
          'http://static.qingmei.me/20180529/0012154437e8918c8bbbb77e7928bf46.jpg/640?sign=89b7922eae367af15cb761a10040de9c&t=5b102a10'
        ],
        votes: {
          count: 999,
          avatarList: [
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272',
            'http://avatar.qingmei.me/1004809/c31895a095baac5a14125a32d35458a483d2273c/64?t=1526982272'
          ]
        },
        comments: [{
          nickname: '爱吃猫粮的鱼',
          content: '谢谢'
        }, {
          nickname: '爱吃猫粮的鱼',
          content: `前几天街上走着，突然一个很漂亮的小姐姐拿着一个手机问我，小哥哥，小哥哥，你看我的手机是不是有什么问题？好像缺点儿什么？我一看是水果最新款，解屏没什么问题，我说，没问题啊？功能很全什么也不缺～这时小姐姐迷之微笑的说，缺你的微信啊？我去居然这么漂亮的小姐姐套路我？我愉快的加了她的微信……结果这几天我才发现，这货是微商……`
        }],
        publishAt: '2018-05-29 10:00:00',
        showToolbar: false
      }]
    }
  },
  methods: {
    leaveComment (record) {
      record.showToolbar = !record.showToolbar
    }
  }
}
</script>

<style lang="scss" scoped>
  .business-record {
    .record {
      padding: 10px 20px;
      .user-info {
        display: flex;
        align-items: center;
        .avatar {
          width: 60px;
          height: 60px;
          border-radius: 100%;
        }
        .nickname {
          font-size: 30px;
          margin-left: 20px;
          color: #55657d;
        }
        .gender {
          margin-left: 10px;
          display: flex;
          align-items: center;
          justify-content: center;
          width: 30px;
          height: 30px;
          border-radius: 100%;
          background: rgb(255, 123, 182);
          img {
            width: 20px;
            height: 20px;
          }
        }
      }
      .content {
        font-size: 30px;
        line-height: 50px;
        margin-left: 76px;
      }
      .imgs {
        display: flex;
        flex-wrap: wrap;
        margin:20px 0 0 76px;
        .img-wrapper {
          width: 210px;
          img {
            width: 200px;
            height: 200px;
          }
        }
      }
      .panel {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin: 20px 16px 0 76px;
        position: relative;
        .publish-at {
          font-size: 24px;
          color: #999;
        }
        .leave-comment {
          width: 40px;
          height: 40px;
        }
        .toolbar {
          background: #4D5154;
          border-radius: 10px;
          font-size: 16px;
          color: #fff;
          display: flex;
          justify-content: center;
          align-items: center;
          width: 200px;
          height: 60px;
          position: absolute;
          right: 50px;
          .like {
            display: flex;
            justify-content: center;
            align-items: center;
            flex: 1;
            &:active {
              background: #4D5154;
            }
            img {
              width: 30px;
              height: 30px;
              margin-left: 10px;
            }
          }
          .review {
            display: flex;
            justify-content: center;
            align-items: center;
            flex: 1;
            img {
              width: 30px;
              height: 30px;
              margin-left: 10px;
            }
          }
        }
      }
      .comments {
        font-size: 28px;
        margin: 10px 0 0 76px;
        line-height: 40px;
        background: #f7f7f7;
        padding: 20px;
        .comment {
          margin-top: 10px;
          .nickname {
            color: #55657d;
          }
        }
        .upvote {
          display: flex;
          align-items: center;
          padding-bottom: 10px;
          border-bottom: 1px solid #eee;
          .count {
            font-size: 24px;
            color: #999;
          }
          .avatar-list {
            flex: 1;
            .avatar {
              width: 40px;
              height: 40px;
              border-radius: 100%;
              margin-left: 10px;
            }
          }
        }
      }
    }
  }
</style>
