<template>
  <b-row class="product">
    <div class="wrap-slider">
      <slider ref="slider" :options="options">
          <slideritem 
            v-for="(banner,index) in banners" 
            :key="index">
              <div class="contain-img">
                <img :src="banner.htmlFirst" />
              </div>
              <div class="contain-img">
                <img :src="banner.htmlSecond" />
              </div>
          </slideritem>
          <div slot="loading">loading...</div>
      </slider>
    </div>
  </b-row>
</template>

<script>
import { VueAgile } from 'vue-agile';
import { slider, slideritem } from 'vue-concise-slider'

export default {
  name:"product",
  data () {
    return {
      banners:[
        { 
          htmlFirst: require('../assets/product/korea_mall.png'),
          htmlSecond: require('../assets/product/korea_mall.png')
        },
        { 
          htmlFirst: require('../assets/product/korea_mall.png'),
          htmlSecond: require('../assets/product/korea_mall.png')
        },
        { 
          htmlFirst: require('../assets/product/korea_mall.png'),
          htmlSecond: require('../assets/product/korea_mall.png') 
        },
        { 
          htmlFirst: require('../assets/product/korea_mall.png'),
          htmlSecond: require('../assets/product/korea_mall.png') 
        },
      ],
      options: {
        currentPage: 2,
        thresholdDistance:'100',
        pagination: false,
        deviation: '1000',
        centeredSlides: false
      }
    }
  },
  components: {
    slider,
    slideritem
  }
}
</script>


<style lang="scss" src="@/assets/scss/_product.scss" scoped></style>
