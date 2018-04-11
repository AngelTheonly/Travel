<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" >
        </swiper-slide>
        <div  class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>  
</template>

<script>
export default {
  name: 'HomeSwiper',
  data (){
      return{
          swiperOption:{
              pagination: '.swiper-pagination',
              loop:true
          },
          swiperList:[
              {
                  id:'0001',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/81/61e16fc667c0bb02.jpg_640x200_ea28d62a.jpg'
              },
              {
                  id:'0002',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/c6/fc5c80d6ee46b402.jpg_640x200_91cad36c.jpg'
              },
          ]
      }
  }
}
</script>

<style lang="scss" scoped>
   
  .wrapper{
      width: 100%;
      overflow: hidden;
      height: 0;
      padding-bottom:31.25%; 
      background-color: #eee;
    .swiper-img{
        width: 100%;
    }
  }
  
</style>

