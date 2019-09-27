<template>
  <div>
    <!-- 搜索 -->
    <div class="search" :class="{focused:focused}">
      <!-- 输入框 -->
      <div class="input-box">
        <input type="text" @focus="goSearch" :placeholder="placeholder" />
        <span class="cancel" @click="cancel">取消</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      focused: false,
      placeholder: ""
    };
  },
  methods: {
    // 点击
    goSearch() {
      this.focused = true;
      this.placeholder = "请输入您想要的商品";
    },
    // 取消
    cancel() {
      this.focused = false;
      this.placeholder = "";
    }
  }
};
</script>

<style scoped lang='less'>
.search {
  padding: 20rpx 18rpx;
  background-color: #eb4450;

  // 搜索状态
  &.focused {
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 9;
    background-color: #eee;
    box-sizing: border-box;
    .input-box {

      .cancel {
        display: block;
        margin-left:  20rpx;
      }
      &::before {
        display: block;
      }
      &:after {
        display: none;
      }
    }
  }
  .input-box {
    display: flex;
    position: relative;

    &::after {
      content: "搜索";
      display: block;
      color: #808080;
      display: block;
      height: 36rpx;
      line-height: 36rpx;
      font-size: 24rpx;
      padding-left: 48rpx;
      background-image: url(https://ugo2.oss-cn-hangzhou.aliyuncs.com/images/icon_search%402x.png);
      background-size: 33rpx;
      background-repeat: no-repeat;

      position: absolute;
      left: 50%;
      top: 50%;
      margin-top: -18rpx;
      margin-left: -47rpx;
    }

    &::before {
      content: "";
      display: none;
      height: 36rpx;
      line-height: 36rpx;
      font-size: 24rpx;
      padding-left: 48rpx;
      background-image: url(https://ugo2.oss-cn-hangzhou.aliyuncs.com/images/icon_search%402x.png);
      background-size: 33rpx;      
      background-repeat: no-repeat;

      position: absolute;
      left: 0%;
      top: 50%;
      margin-left: 20rpx;
      margin-top: -18rpx;
    }
    // 取消按钮
    .cancel {
      display: none;
      width: 160rpx;
      height: 59rpx;
      text-align: center;
      line-height: 59rpx;
      border: 1px solid #c4c4c4;
      background-color: #eeeeee;
      border-radius: 6rpx;
    }

    input {
      flex: 1;
      height: 60rpx;
      background-color: #ffffff;
      border-radius: 5rpx;
      padding-left: 70rpx;
    }
  }
}
</style>