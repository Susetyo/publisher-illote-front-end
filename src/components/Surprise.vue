<template>
  <b-row
    class="new_arrival">
    <div class="header">
      <img :src="headerImg" />
    </div>
    <div class="wrap-slider">
      <img
        :style="{width:'100%'}"
        :src="contentImg" />
    </div>
  </b-row>
</template>

<script>
import { VueAgile } from 'vue-agile';
import { slider, slideritem } from 'vue-concise-slider'

export default {
  name:"Surprise",
  data () {
    return {
      headerImg:require('../assets/surprise/surprise.png'),
      contentImg: require('../assets/surprise/nb_surprise.png'),
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


<style lang="scss" src="@/assets/scss/_newarrival.scss" scoped></style>
