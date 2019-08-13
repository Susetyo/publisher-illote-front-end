<template>
  <b-row class="new_arrival">
    <div class="header">
      <img :src="headerImg" />
    </div>
    <div class="wrap-slider">
      <slider ref="slider" :options="options">
          <slideritem 
            v-for="(banner,index) in banners" 
            :key="index">
              <a class="link_new_arrival">
                <div class="item">
                  <div class="item-img">
                    <img :src="banner.htmlFirst.url"/>
                  </div>
                  <div class="item-content">
                    <div class="new_arrival-title">{{banner.htmlFirst.title}}</div>
                    <div class="new_arrival-content">
                      <div class="new_arrival-content__wrapper">
                        <div class="new_arrival-content__icon">
                          <font-awesome-icon
                            icon="clock"
                            class="font-awesome"
                          />
                        </div>
                        <div class="new_arrival-content__data">{{banner.htmlFirst.desc}}</div>
                      </div>
                      <div class="new_arrival-content__wrapper">
                        <div class="mt10 new_arrival-content__icon"> 
                          <font-awesome-icon
                            icon="map-marker-alt"
                            class="font-awesome"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="row">
                      <div class="new_arrival-status col align-self-end">
                        {{banner.htmlFirst.price}}
                      </div>
                    </div>
                  </div>
                </div>
              </a>
              <a class="link_new_arrival">
                <div class="item">
                  <div class="item-img">
                    <img :src="banner.htmlSecond.url"/>
                  </div>
                  <div class="item-content">
                    <div class="new_arrival-title">{{banner.htmlSecond.title}}</div>
                    <div class="new_arrival-content">
                      <div class="new_arrival-content__wrapper">
                        <div class="new_arrival-content__icon">
                          <font-awesome-icon
                            icon="clock"
                            class="font-awesome"
                          />
                        </div>
                        <div class="new_arrival-content__data">{{banner.htmlSecond.desc}}</div>
                      </div>
                      <div class="new_arrival-content__wrapper">
                        <div class="mt10 new_arrival-content__icon"> 
                          <font-awesome-icon
                            icon="map-marker-alt"
                            class="font-awesome"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="row">
                      <div class="new_arrival-status col align-self-end">
                        {{banner.htmlSecond.price}}
                      </div>
                    </div>
                  </div>
                </div>
              </a>
              <a class="link_new_arrival">
                <div class="item">
                  <div class="item-img">
                    <img :src="banner.htmlSecond.url"/>
                  </div>
                  <div class="item-content">
                    <div class="new_arrival-title">{{banner.htmlSecond.title}}</div>
                    <div class="new_arrival-content">
                      <div class="new_arrival-content__wrapper">
                        <div class="new_arrival-content__icon">
                          <font-awesome-icon
                            icon="clock"
                            class="font-awesome"
                          />
                        </div>
                        <div class="new_arrival-content__data">{{banner.htmlSecond.desc}}</div>
                      </div>
                      <div class="new_arrival-content__wrapper">
                        <div class="mt10 new_arrival-content__icon"> 
                          <font-awesome-icon
                            icon="map-marker-alt"
                            class="font-awesome"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="row">
                      <div class="new_arrival-status col align-self-end">
                        {{banner.htmlSecond.price}}
                      </div>
                    </div>
                  </div>
                </div>
              </a>

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
  name:"NewArrival",
  data () {
    return {
      headerImg:require('../assets/new_arrival/new_arrival_header.png'),
      banners:[
        { 
          htmlFirst: { 
            url: require('../assets/new_arrival/bts_map_soul.png'),
            title: 'Big Hit Entertain',
            desc: 'BTS MAP OF SOUL',
            price: '222.000'
          },
          htmlSecond: { 
            url: require('../assets/new_arrival/makeup_case.png'),
            title: 'Masami Shouko',
            desc: 'Masami Shouko 7',
            price: '194.700'
          } 
        },
        { 
          htmlFirst: { 
            url: require('../assets/new_arrival/bts_map_soul.png'),
            title: 'Big Hit Entertain',
            desc: 'BTS MAP OF SOUL',
            price: '222.000'
          },
          htmlSecond: { 
            url: require('../assets/new_arrival/makeup_case.png'),
            title: 'Masami Shouko',
            desc: 'Masami Shouko 7',
            price: '194.700'
          } 
        },
        { 
          htmlFirst: { 
            url: require('../assets/new_arrival/bts_map_soul.png'),
            title: 'Big Hit Entertain',
            desc: 'BTS MAP OF SOUL',
            price: '222.000'
          },
          htmlSecond: { 
            url: require('../assets/new_arrival/makeup_case.png'),
            title: 'Masami Shouko',
            desc: 'Masami Shouko 7',
            price: '194.700'
          } 
        },
        { 
          htmlFirst: { 
            url: require('../assets/new_arrival/bts_map_soul.png'),
            title: 'Big Hit Entertain',
            desc: 'BTS MAP OF SOUL',
            price: '222.000'
          },
          htmlSecond: { 
            url: require('../assets/new_arrival/makeup_case.png'),
            title: 'Masami Shouko',
            desc: 'Masami Shouko 7',
            price: '194.700'
          } 
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


<style lang="scss" src="@/assets/scss/_newarrival.scss" scoped></style>
