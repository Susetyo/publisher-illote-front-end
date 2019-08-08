<template>
  <b-row class="discount">
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
  name:"discount",
  data () {
    return {
      banners:[
        { 
          htmlFirst: require('../assets/discount/monday_deal.png'),
          htmlSecond: require('../assets/discount/thursday_deal.png') 
        },
        { 
          htmlFirst: require('../assets/discount/monday_deal.png'),
          htmlSecond: require('../assets/discount/thursday_deal.png') 
        },
        { 
          htmlFirst: require('../assets/discount/monday_deal.png'),
          htmlSecond: require('../assets/discount/thursday_deal.png') 
        },
        { 
          htmlFirst: require('../assets/discount/monday_deal.png'),
          htmlSecond: require('../assets/discount/thursday_deal.png') 
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


<style lang="scss" src="@/assets/scss/_discount.scss" scoped></style>
