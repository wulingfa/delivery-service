<template>
  <div class="docker">
    <div
       v-for="(item,index) in dockerList"
       :class="{'docker_item':true, 'docker_item--active': index === 0}"
       class="docker_item "
       :key="item.icon"
    >
      <div class="iconfont" v-html="item.icon"/>
      <div class="docker_title"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Docker',
  setup () {
    const dockerList = [
      { icon: '&#xe813;', text: '首页' },
      { icon: '&#xe638;', text: '购物车' },
      { icon: '&#xe61e;', text: '订单' },
      { icon: '&#xe662;', text: '我的' }
    ]
    return { dockerList }
  }

}

</script>

<style lang="scss" scoped>
.docker {
  @import "../../style/viriables.scss";
  display: flex;
  box-sizing: border-box;
  position: absolute;
  padding: 0.18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 0.01rem solid $content-bgColor;
  color: $content-fontcolor;
  &_item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.08rem 0 0.02rem;
      font-size: 0.2rem;
    }
    &--active {
      color: #1fa4fc;
    }
  }
  &_title {
    font-size: 20px;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>
