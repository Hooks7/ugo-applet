<template>
  <div :style="{height:windowHeight,overflow:'hidden'}">
    <!-- 搜索 -->
    <search @search="disableScroll" />
    <!-- 轮播图 -->
    <swiper
      indicator-dots
      indicator-color="rgba(255,255,255,3)"
      indicator-active-color="#ccc"
      autoplay
      circular
      interval="3000"
    >
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner1.png" alt />
        </a>
      </swiper-item>
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner2.png" alt />
        </a>
      </swiper-item>
      <swiper-item>
        <a href>
          <img src="/static/uploads/banner3.png" alt />
        </a>
      </swiper-item>
    </swiper>

    <!-- 主导航 -->
    <div class="nav">
      <a href>
        <img src="/static/uploads/icon_index_nav_4@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_3@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_2@2x.png" alt />
      </a>
      <a href>
        <img src="/static/uploads/icon_index_nav_1@2x.png" alt />
      </a>
    </div>

    <!-- 楼层 -->
    <div class="floors">
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor01_title.png" alt />
        </div>
        <!-- 类别 -->
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor01_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor01_5@2x.png" alt />
          </a>
        </div>
      </div>
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor02_title.png" alt />
        </div>
        <!-- 类别 -->
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor02_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor02_5@2x.png" alt />
          </a>
        </div>
      </div>
      <div class="floor">
        <!-- 标题 -->
        <div class="title">
          <img src="/static/uploads/pic_floor03_title.png" alt />
        </div>
        <!-- 类别 -->
        <div class="items">
          <a href>
            <img src="/static/uploads/pic_floor03_1@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_2@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_3@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_4@2x.png" alt />
          </a>
          <a href>
            <img src="/static/uploads/pic_floor03_5@2x.png" alt />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import search from "@/components/search";

export default {
  data() {
    return {
      windowHeight: "auto"
    };
  },

  components: {
    search
  },

  methods: {
    disableScroll(ev) {
      console.log(ev);
      this.windowHeight = ev.windowHeight;
    }
  },

  created() {
    // let app = getApp()
  }
};
</script>

<style scoped lang='less'>
swiper {
  height: 340rpx;
  a {
    width: 100%;
    height: 100%;
  }
}
.nav {
  display: flex;
  justify-content: space-between;
  height: 193rpx;
  align-items: center;
  padding: 0 30rpx;
  a {
    display: block;
    width: 128rpx;
    height: 140rpx;
  }
}

.floors {
  .floor {
    .title {
      height: 90rpx;
      background-color: #f4f4f4;
      padding: 32rpx 0 0 14rpx;
    }
    .items {
      padding: 20rpx 16rpx;
      overflow: hidden;
    }
    &:first-child {
      .items {
        a {
          width: 233rpx;
          height: 188rpx;
        }
        a:first-child {
          width: 233rpx;
          height: 386rpx;
        }
      }
    }

    a {
      float: left;
      margin-left: 10rpx;
    }

    a:first-child {
      width: 232rpx;
      height: 386rpx;
      margin-left: 0;
    }
    a:nth-child(2),
    a:nth-child(5) {
      width: 273rpx;
      height: 188rpx;
    }
    a:nth-child(3),
    a:nth-child(4) {
      width: 193rpx;
      height: 188rpx;
    }

    a:nth-last-child(-n + 2) {
      margin-top: 10rpx;
    }
  }
}
</style>
