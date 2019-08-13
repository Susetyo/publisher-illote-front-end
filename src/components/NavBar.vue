<template>
<div>
  <b-navbar
    :class="{ scrolling: scrollPosition > 371 }"
    class="nav_cm" 
    toggleable="lg" 
    type="light">

    <div :style="{ 
      paddingTop: '10px',
      backgroundColor: 'transparent', 
      width:'100%',
      position: 'fixed',
      left:0,
      top:0,
      display:'flex',
      zIndex: 10
    }">
      
      <button data-v-4295d220="" type="button" aria-label="Toggle navigation" aria-controls="nav-collapse" aria-expanded="false" class="navbar-toggler">
        <span class="navbar-toggler-icon"></span>
      </button>
      
      <b-nav-form>
        <b-input-group>
          <b-input-group-text slot="append" 
          style="background-color: white;
            border-left: 0px;
            border-top-right-radius: 25px;
            border-bottom-right-radius: 25px;">
            <i class="fas fa-search"></i>
          </b-input-group-text>
          <b-form-input 
            style="background-color: white;
            border-right: 0px;
            border-top-left-radius: 25px;
            border-bottom-left-radius: 25px;"></b-form-input>
        </b-input-group>
      </b-nav-form>
    </div>  
    <div class="search-background" :style="{ opacity:theOpacity }"></div>
  </b-navbar>
    
</div>
</template>
<style lang="scss" src="@/assets/scss/_nav.scss" scoped></style>



<script>
export default {
  name:"NavBar",
  data() {
    return {
      scrollPosition: null,
      theOpacity: 0
    };
  },
  methods:{
    updateScroll() {
      this.scrollPosition = window.scrollY;
      this.theOpacity = window.scrollY == 0 ? 0 : window.scrollY / 1000;
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  }
};
</script>

<style lang="scss" scoped>
.navbar-light .navbar-toggler{
  border-color: transparent !important;
}
.scrolling{
  background-color: white;
}
</style>

