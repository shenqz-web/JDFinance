<template lang="html">
  <panel title="新品推荐" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.arrow">更多监护></div>
      <slider :options="options" :items="items" cname="product-slider"></slider>
    </section>
  </panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from '../core/slider.vue'
export default {
  components: {
    Panel,
    Slider
  },
  data () {
    return {
      options: {
        slidesPerView: 2.3,
        spaceBetween: 30,
        freeMode: true
      },
      items: [{
        href: "home",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t17692/108/1667948905/47352/b3b5fec5/5ad4077bN829fc64d.jpg?width=335&height=421",
      }, {
        href: "home",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t17017/315/1681990516/35892/46d5d0e/5ad40797Nd8624d82.jpg?width=335&height=421",
      }, {
        href: "home",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t17977/1/1701720589/44385/219809f6/5ad407a8N8feeb421.jpg?width=335&height=421",
      }, {
        href: "home",
        src: "//img12.360buyimg.com/jrpmobile/jfs/t18598/49/1683491486/34072/cb622afa/5ad407b7N95527875.jpg?width=335&height=421",
      }]
    }
  }
}
</script>

<style lang="scss">
  .product-slider{
    .swiper-container{
      box-sizing: border-box;
      padding: 0 24px;
      .swiper-slide{
        a{
          display: inline-block;
          width: 100%;
          img{
            width: 100%;
            display: block;
            height: 314px;
            border: 1px solid #fafafa;
          }
        }
      }
    }
  }
</style>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  .content{
    padding-bottom: 40px;
    position: relative;
    .arrow{
      position: absolute;
      top: -70px;
      right: 20px;
      font-size: 28px;
      color: #999;
    }
  }
}
</style>
