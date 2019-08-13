<template>
  <div class="art_board">

    <div class="row art_board__wraper">
      <div
        v-for="(item,index) in items"
        :key="'sec-'+index"
        v-if ="index<5" 
        class="art_board__wraper__container">

          <span>
            <img :src="item.url" />
          </span>
          <span class="title" > {{ item.title }} </span>

      </div>

    </div>

    <div class="row art_board__wraper">
      <div 
        v-for="(item,index) in items"
        :key="'sec-'+index"
        v-if ="index<10 && index>4" 
        class="art_board__wraper__container">
          <span>
            <img
              v-if="item.title == `K-Wave`"
              :style="{ height: '44px', width: '57px' }"  
              :src="item.url" />
            <img
              v-else 
              :src="item.url" />
          </span>
          <span class="title">{{ item.title }}</span>
        </div>
      </div>
      
    </div>

  </div>
</template>

<script>
export default {
  name:"ArtBoard",
  data () {
    return {
      items:[
        { 
          title: 'Fashion',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_fashion.png'
        },
        { 
          title: 'Beauty & Health',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_beauty.png'
        },
        {
          title: 'Mom & Kids',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_momkids.png'
        },
        {
          title: 'Electronic & Living',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_electronic.png'
        },
        { 
          title: 'Sport & Hobby',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_sport.png'
        },
        { 
          title: 'Groceries & Services',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_groceries.png'
        },
        { 
          title: 'Pulsa',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_pulsa.png'
        },
        { 
          title: 'Promo',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_promo.png'
        },
        { 
          title: 'K-Wave',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_kwave.png'
        },
        { 
          title: 'iLotte Free',
          url: 'https://cdn.ilotte.me/static/mp/819/static-root/images/icon/ilotte/icon_cat_free.png'
        },
      ]
    }
  },
  computed:{
    wrapperLoop: function(){
      return Math.ceil(this.items.length)/5;
    }
  }
}
</script>

<style lang="scss" src="@/assets/scss/_artboard.scss" scoped></style>
