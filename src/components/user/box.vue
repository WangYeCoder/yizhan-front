<template>
  <div class="page">

  </div>
</template>

<script>
  export default {
    name: "Box",
    props: {
      title: String,
      visible: {
        type: Boolean,
        default: false
      }
    },
    data() {
      return {
        motto: 123123,
        userInfo: {}
      };
    },
    component:{
    },
    methods: {
      change: function() {
        this.motto = 1;
      },
      getUserInfo() {
        // 调用登录接口
        wx.login({
          success: () => {
            wx.getUserInfo({
              success: (res) => {
                this.userInfo = res.userInfo;
              }
            });
          }
        });
      }
    },
    mounted: function() {

      this.getUserInfo();
    }

  };
</script>

<style>
  .userinfo {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .userinfo-avatar {
    position: absolute;
    width: 80rpx;
    height: 80rpx;
    margin: 20rpx;
    border-radius: 50%;
    top: 0;
    right: 0;

  }

  .userinfo-nickname {
    color: #aaa;
    font-size: 14px;
  }

  .usermotto {
    margin-top: 150px;
  }

  .form-control {
    display: block;
    padding: 0 12px;
    margin-bottom: 5px;
    border: 1px solid #ccc;
  }

  .counter {
    display: inline-block;
    margin: 10px auto;
    padding: 5px 10px;
    color: blue;
    border: 1px solid blue;
  }
</style>
