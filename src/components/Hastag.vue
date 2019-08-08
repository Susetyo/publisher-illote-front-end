<template>
  <b-row class="hastag">
      <img :src="hastag_img" />
  </b-row>
</template>

<script>
export default {
  name:"hastag",
  data () {
    return {
      hastag_img: require('../assets/hastag/hastag_mall_dari_hape.png')
    }
  }
}
</script>

<style lang="scss" src="@/assets/scss/_hastag.scss" scoped></style>
