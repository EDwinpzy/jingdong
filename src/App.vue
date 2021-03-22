<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe604;</span>
      北京理工大学BEM_CSS命名规则，__表示子元素，--表示状态
      BEM_CSS命名规则，__表示子元素，--表示状态
      BEM_CSS命名规则，__表示子元素，--表示状态
      BEM_CSS命名规则，__表示子元素，--表示状态
      BEM_CSS命名规则，__表示子元素，--表示状态
      <span class="iconfont position__notice">&#xe6bb;</span>
    </div>
  </div>
  <div class="docker">
    <!-- BEM_CSS命名规则，__表示子元素，--表示状态 -->
    <div class="docker__item docker__item--active">
      <div class="iconfont">&#xe616;</div>
      <div class="docker__title">首页</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe600;</div>
      <div class="docker__title">购物车</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe60c;</div>
      <div class="docker__title">订单</div>
    </div>
    <div class="docker__item">
      <div class="iconfont">&#xe607;</div>
      <div class="docker__title">我的</div>
    </div>
  </div>
</template>

<style lang="scss">
@import "./style/viriables.scss";
@import './style/mixins.scss';
.position {
  padding: 0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  //这样写优先级高
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.18rem;
  }
  .position__notice {
    position: absolute;
    top: 0.17rem;
    right: 0.14rem;
    font-size: 0.22rem;
  }
  color: content-fontcolor;
}
.wrapper {
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.5rem;
  right: 0;
  padding: 0 0.18rem;
}
.docker {
  /* 将布局定义成容器 */
  display: flex;
  /* 盒模型，以容器的外边框作为长和宽（最外层） */
  box-sizing: border-box;
  /* 设置内边距(上下 左右) */
  position: absolute;
  padding: 0 0.18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  /* 边框样式 */
  border-top: 0.01rem solid #f1f1f1;
  color: content-fontcolor;
  &__item {
    /* 自适应 */
    flex: 1;
    text-align: center;
    /* docker__item下的iconfont样式 */
    .iconfont {
      /* 图标上下间距(上右下左) */
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &--active {
      color: #1fa4fc;
    }
  }
  &__title {
    font-size: 0.2rem;
    /* 缩放 */
    transform: scale(0.5, 0.5);
    /* 缩放中心点 */
    transform-origin: center top;
  }
}
</style>
