<template>
<div>
  <b-navbar
    :class="{ scrolling: scrollPosition > 371 }"
    class="nav_cm" 
    toggleable="lg" 
    type="light">

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Link</b-nav-item>
        <b-nav-item href="#" disabled>Disabled</b-nav-item>
      </b-navbar-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item-dropdown>
          <template slot="button-content"><em>User</em></template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
    
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
    };
  },
  methods:{
    updateScroll() {
      this.scrollPosition = window.scrollY;
      console.log(this.scrollPosition)
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  }
};
</script>

<style lang="scss" scoped>
.navbar-light .navbar-toggler{
  background-color: white;
}
.scrolling{
  background-color: white;
}
</style>

