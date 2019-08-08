<template>
  <b-row class="banner">
    <div class="wrap-slider">
      <slider ref="slider" :options="options">
          <slideritem 
            v-for="(banner,index) in banners" 
            :key="index">
              <img :src="banner.html" />
          </slideritem>
          <div slot="loading">loading...</div>
      </slider>
    </div>
  </b-row>
</template>

<script>
let img_banner_url = require('../assets/banner/big.png');

import { VueAgile } from 'vue-agile';
import { slider, slideritem } from 'vue-concise-slider'

export default {
  name:"banner",
  data () {
    return {
      banners:[
        { html: img_banner_url },
        { html: img_banner_url },
        { html: img_banner_url }
      ],
      options: {
        currentPage: 0,
        autoplay:'2000',
        loop: true,
        pagination: false,
      }
    }
  },
  components: {
    slider,
    slideritem
  }
}
</script>


<style lang="scss" src="@/assets/scss/_banner.scss" scoped></style>
