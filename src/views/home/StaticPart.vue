<template>
  <div class="position">
    <span class="iconfont position__icon">&#xe624;</span>
    南京工业职业技术大学计算机与软件学院软件工程2126
    <span class="iconfont position__notice">&#xe63f;</span>
  </div>
  <!-- 搜索区 -->
  <div class="search">
    <span class="iconfont">&#xe625;</span>
    <span class="search__text">山姆会员店优惠商品</span>
  </div>
  <!-- banner -->
  <div class="banner">
    <img
      src="http://47.103.107.137:9000/jingdong/banner.jpeg"
      class="banner__img"
    />
  </div>
  <!-- icons -->
  <div class="icons">
    <div class="icons__item" v-for="item in iconsList" :key="item.desc">
      <img
        :src="`http://47.103.107.137:9000/jingdong/${item.imgName}.png`"
        class="icons__item__img"
      />
      <p class="icons__item__desc">{{ item.desc }}</p>
    </div>
  </div>
  <!-- 分割线 -->
  <div class="gap"></div>
  <!-- 附近店铺 -->
  <div class="nearby">
    <h3 class="nearby__title">附近店铺</h3>
    <div class="nearby__item">
      <img
        src="https://ossstored.oss-cn-shanghai.aliyuncs.com/img/jingdong/shop1.png"
        class="nearby__item__img"
      />
      <div class="nearby__content">
        <div class="nearby__content__title">沃尔玛</div>
        <div class="nearby__tags">
          <span class="nearby__content__tag">月售1万+</span>
          <span class="nearby__content__tag">起送￥0</span>
          <span class="nearby__content__tag">基础运费</span>
        </div>
        <div class="nearby__content__highlight">
          VIP尊享满99元减4元运费卷（每月3张）
        </div>
      </div>
    </div>
    <div class="nearby__item">
      <img
        src="https://ossstored.oss-cn-shanghai.aliyuncs.com/img/jingdong/shop2.png"
        class="nearby__item__img"
      />
      <div class="nearby__content">
        <div class="nearby__content__title">山姆会员店</div>
        <div class="nearby__tags">
          <span class="nearby__content__tag">月售1万+</span>
          <span class="nearby__content__tag">起送￥0</span>
          <span class="nearby__content__tag">基础运费￥5</span>
        </div>
        <div class="nearby__content__highlight">联合利华洗护满10减5</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StaticPart",
  setup() {
    const iconsList = [
      { imgName: "超市", desc: "超市便利" },
      { imgName: "菜市场", desc: "菜市场" },
      { imgName: "水果店", desc: "水果店" },
      { imgName: "鲜花", desc: "鲜花绿植" },
      { imgName: "医药健康", desc: "医药健康" },
      { imgName: "家居", desc: "家居时尚" },
      { imgName: "蛋糕", desc: "烘培蛋糕" },
      { imgName: "签到", desc: "签到" },
      { imgName: "大牌免运", desc: "大牌免运" },
      { imgName: "红包", desc: "红包套餐" },
    ];
    return { iconsList };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/virables.scss";
@import "@/style/mixins.scss";

.position {
  position: relative;
  padding: 0.16rem 0.16rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipse;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position__notice {
    position: absolute;
    right: 0;
    top: 0.17rem;
    font-size: 0.2rem;
  }
  color: $content-fontcolor;
}
.search {
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background-color: $search-bgColor;
  color: $search-fontColor;
  border-radius: 0.16rem;
  .iconfont {
    display: inline-block;
    padding: 0 0.08rem 0 0.16rem;
    font-style: 0.16rem;
  }
  &__text {
    display: inline-block;
    font-size: 0.14rem;
  }
}
.banner {
  height: 0;
  overflow: hidden;
  // hack技巧，预留高度防抖（图片高/图片宽）
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}

.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    width: 20%;
    margin-bottom: 0.1rem;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0.06rem 0.06rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
}
.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background-color: $content-bgColor;
}

.nearby {
  &__title {
    margin: 0.16rem 0 0.02rem 0;
    font-size: 0.18rem;
    font-weight: normal;
    color: $dark-fontColor;
  }

  &__item {
    display: flex;
    padding-top: 0.12rem;
    &__img {
      margin-right: 0.16rem;
      width: 0.56rem;
      height: 0.56rem;
    }
  }
  &__content {
    flex: 1;
    padding-bottom: 0.12rem;
    border: 1px solid $content-bgColor;
    &__title {
      line-height: 0.22rem;
      font-size: 0.16rem;
      color: $content-fontcolor;
    }
    &__tags {
      margin-top: 0.08rem;
      line-height: 0.18rem;
      font-size: 0.13rem;
      color: $content-bgColor;
    }
    &__tag {
      margin-right: 0.16rem;
    }
    &__highlight {
      margin: 0.08rem 0 0 0;
      line-height: 0.18rem;
      font-size: 0.13rem;
      color: #e93b3b;
    }
  }
}
</style>