<template>
  <div>
    <!-- 搜索 -->
    <search/>
    <!-- 轮播图 -->
    <swiper
      indicator-dots
      indicator-color="rgba(255,255,255,3)"
      indicator-active-color="#ccc"
      autoplay
      circular
      interval='3000'
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
  </div>
</template>

<script>
import search from "@/components/search";

export default {
  data() {
    return {};
  },

  components: {

    search
  },

  methods: {},

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
</style>
