<template>
  <div class="icons">
     <swiper class="swiper" :options="swiperOption">
          <swiper-slide v-for="(page,index) of pages" :key="index">
            <div class="icon" v-for="item of page" :key="item.id">
                <div class="icon-img"> <img :src="item.imgUrl" alt=""></div>
                <p class="icon-desc">{{item.desc}}</p>
            </div>
          </swiper-slide>  
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data (){
      return{
          iconList:[
              {
                  id:'001',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                  desc:'景点门票'
              },
              {
                  id:'002',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
                  desc:'踏青赏花'
              },
              {
                  id:'003',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
                  desc:'演出'
              },
              {
                  id:'004',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/c1/ac058f238b9a6802.png',
                  desc:'一日游'
              },
              {
                  id:'005',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
                  desc:'必游榜单'
              },
              {
                  id:'006',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
                  desc:'动植物园'
              },
              {
                  id:'007',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
                  desc:'名胜古迹'
              },
              {
                  id:'008',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
                  desc:'公园'
              },
              {
                  id:'009',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
                  desc:'自然风光'
              },
              {
                  id:'010',
                  imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
                  desc:'全部玩乐'
              }
          ],
           swiperOption:{}
      }
  },
  computed:{
      pages () {
          const pages= [];
          this.iconList.forEach((item,index) => {
              const page = Math.floor(index / 8)
              if(!pages[page]){
                  pages[page]=[]
              }
              pages[page].push(item)
          })
          return pages
      }
  }
}
</script>

<style lang="scss" scoped>
   @import '~styles/varibles.scss';
  .icons{
      overflow: hidden;
      height: 0;
      padding-bottom: 50%;
      .swiper{
          overflow: hidden;
          height: 0;
          padding-bottom: 50%;
      }
      .icon{
          overflow: hidden;
          float: left;
          width: 25%;
          height: 0;
          padding-bottom: 25%;
          position: relative;
          .icon-img{
              position: absolute;
              top: 0;
              left: 0;
              right: 0;
              bottom: .1rem;
              box-sizing: border-box;
              padding: .1rem;
              display: flex;
              img{
                  display: block;
                  margin: auto;
                  width: 65%;
              }
          }
          .icon-desc{
             position: absolute;
              left: 0;
              right: 0;
              bottom: 0;
              height: .44rem;
              line-height: .44rem;
              color:$darkTextColor;
              text-align: center;
              @include ellipsis()
          } 
      }
  }
</style>


