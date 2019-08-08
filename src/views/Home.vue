<template>
  <div>
    <nav-bar></nav-bar>
    <b-container fluid>
      <banner></banner>
      <hastag></hastag>
      <art-board></art-board>
      <discount></discount>
      <new-arrival></new-arrival>
      <product></product>
      <surprise></surprise>
    </b-container>
  </div>
</template>

<script>
import NavBar from '../components/NavBar';
import Banner from '../components/Banner';
import Hastag from '../components/Hastag';
import ArtBoard from '../components/ArtBoard';
import Discount from '../components/Discount';
import NewArrival from '../components/NewArrival';
import Product from '../components/Product';
import Surprise from '../components/Surprise';

export default {
  name: 'home',
  components: {
    ArtBoard,
    NavBar,
    Banner,
    Hastag,
    Discount,
    NewArrival,
    Product,
    Surprise
  },
};
</script>
<style lang="scss" scoped>
.container-fluid{
  background-color:#d4d0cf
}
</style>
