<template>
  <div class="wrapper">
    <!-- 定位区 -->
    <div class="wrapper__position">
      <span class="iconfont">&#xe624;</span>
      南京工业职业技术大学计算机与软件学院软件工程2126
      <span class="iconfont position__notice">&#xe63f;</span>
    </div>


  <!-- 底部导航 -->
  <div class="docker">
    <!-- BEM block__element-modifier -->
    <div class="docker__item docker__item--active">
      <div class="iconfont">&#xe60a;</div>
      <div class="docker__title">首页</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe600;</div>
      <div class="docker__title">购物车</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe610;</div>
      <div class="docker__title">订单</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe78b;</div>
      <div class="docker__title">我的</div>
    </div>
  </div>
</template>

<style lang="scss">
// @import "./style/virables.scss";
@import "./style/index.scss";

.wrapper {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0.5rem;
  padding: 0 0.18rem;
  &__position {
    position: relative;
    padding: 0.16rem 0.16rem 0.16rem 0;
    font-size: 0.16rem;
    @include ellipse;
    .iconfont {
      font-size: 0.2rem;
    }

    .position__notice {
      position: absolute;
      right: 0;
    }
    color: $content-fontcolor;
  }
  &__search {
    margin-bottom: 0.12rem;
    line-height: 0.32rem;
    background-color: $background-color;
    color: $placeholder-color;
    border-radius: 0.16rem;
    .iconfont {
      display: inline-block;
      padding: 0 0.12rem 0 0.16rem;
      font-style: 0.2rem;
    }
    &__text {
      display: inline-block;
      font-size: 0.14rem;
    }
  }
  &__banner {
    height: 0;
    overflow: hidden;
    // hack技巧，预留高度防抖（图片高/图片宽）
    padding-bottom: 25.4%;
    &__img {
      width: 100%;
    }
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
    p {
      margin: 0.06rem 0.06rem 0.06rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
}

.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background-color: $border-color;
}

.docker {
  display: flex;
  position: absolute;
  left: 0;
  bottom: 0;
  padding: 0 0.18rem;
  box-sizing: border-box;
  width: 100%;
  height: 0.49rem;
  border-top: 0.01rem solid $border-color;
  color: $content-fontcolor;
  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &--active {
      color: $highlight-color;
    }
  }
  &__title {
    font-size: 0.2rem;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>
