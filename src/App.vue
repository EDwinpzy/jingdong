<template>
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
.docker {
  /* 将布局定义成容器 */
  display: flex;
  /* 盒模型，以容器的外边框作为长和宽（最外层） */
  box-sizing: border-box;
  /* 设置内边距(上右下左) */
  position: absolute;
  padding: 0 .18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: .49rem;
  /* 边框样式 */
  border-top: 1px solid #F1F1F1;
  &__item {
    /* 自适应 */
    flex: 1;
    text-align: center;
    /* docker__item下的iconfont样式 */
    .iconfont {
      /* 图标上下间距(上右下左) */
      margin: .07rem 0 .02rem 0;
      font-size: .18rem;
    };
    &--active {
      color: #1FA4FC;
    };
  }
  &__title {
    font-size: 20px;
    /* 缩放 */
    transform: scale(.5, .5);
    /* 缩放中心点 */
    transform-origin: center top;
  }
}
</style>
