<template>
  <div class="art_board">

    <div class="row art_board__wraper">
      <div
        v-for="(item,index) in items"
        :key="'sec-'+index"
        v-if ="index<5" 
        class="art_board__wraper__container">

          <span>
            <img src="https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg" />
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
            <img src="https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg" />
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
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'Beauty & Health',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        {
          title: 'Mom & Kids',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        {
           title: 'Electronic & Living',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'Sport & Hobby',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'Groceries & Services',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'Pulsa',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'Promo',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'K-Wave',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
        },
        { 
          title: 'iLotte Free',
          url: 'https://cdn.ilotte.me/static/mp/815/static-root/images/common/no_img_124x124.jpg'
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
