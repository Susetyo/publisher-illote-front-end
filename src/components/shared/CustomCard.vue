<template>
    <a class="link-event">
      <div class="item">
        <div class="item-img">
          <img :src="'https://placekitten.com/1000/300'"/>
        </div>
        <div class="item-content">
          <div class="event-title">Coba</div>
          <div class="event-content">
            <div class="event-content__wrapper">
              <div class="event-content__icon">
                <font-awesome-icon
                  icon="clock"
                  class="font-awesome"
                />
              </div>
              <div class="event-content__data">date</div>
            </div>
            <div class="event-content__wrapper">
              <div class="mt10 event-content__icon"> 
                <font-awesome-icon
                  icon="map-marker-alt"
                  class="font-awesome"
                />
              </div>
              <div class="mt10 event-content__data">
                venue
              </div>
            </div>
          </div>
          <div class="row">
            <div class="event-status">
              currency
            </div>
          </div>
        </div>
      </div>
    </a>
</template>
<script>

export default {
  name: "custom-card",
  props:{
    event:{
      type: Object
    },
    lengthTitle:{
      type: Number
    },
    theNumber:{
      type:Number
    }
  },
}
</script>
<style lang="scss" scoped>
  @import url("https://fonts.googleapis.com/css?family=Varela+Round");
  @import url("https://fonts.googleapis.com/css?family=Lato");

  .link-event {
    text-decoration: none;
    z-index: 1;
  }

  .item {
    margin: 0px;
    background: #ffffff;
    border-radius: 4px;
    min-height: 300px;
    box-shadow: rgba(0, 0, 0, 0.15) 0px 1px 4px 0px;
  }

  .item-img {
    width:100%;
    img {
      width: 100%;
      height: 100px;
      object-fit: cover;
    }
  }

  .item-content {
    padding: 10px 18px;
    text-align: left;
  }

  .event-content {
    margin-top: 15px;
    font-size: 12px;
    color: #9a9a9a;
    min-height: 67px;
  }

  .event-content__wrapper {
    display: flex;
  }

  .event-content__icon {
    margin-left: 0px;
    width: 15px;
  }

  .event-content__data {
    margin-left: 7px;
  }

  .event-title {
    font-size: 14px;
    font-weight: bold;
    color: #323c47;
    min-height: 50px;
  }

  .event-content {
    margin-top: 15px;
    font-size: 10px;
    color: #9a9a9a;
    min-height: 70px;
  }

  .event-status {
    font-family: "Lato", sans-serif;
    font-style: normal;
    font-weight: 800;
    font-size: 18px;
    color: #fcb031;
    padding: 30px 0px 0px 12px;
    text-align: right;
  }
  
  .event-status-label {
    font-family: "Lato", sans-serif;
    font-style: normal;
    font-size: 11px;
    text-align: right;
    color: black;
    padding: 30px 0px 12px 0px;
  }

  .font-awesome {
    margin-right: 6px;
  }

  .mt10 {
    margin-top: 10px;
  }
</style>

