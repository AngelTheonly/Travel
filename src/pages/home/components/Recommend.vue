<template>
  <div>
    <div class="tlitle"> 热销推荐 </div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
      return{
          recommendList:[
              {
              id:'001',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1411/1a/5582f9f24bc50b475a8cbda4c5ac8d24.water.jpg_110x110_95677b58.jpg',
              title:'秦始皇陵博物院（兵马俑）',
              desc:'位于陕西省西安市临潼处...'
             },
              {
              id:'002',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1411/67/272c374a876b2f9ec9860551c993c521.water.jpg_200x200_6d9f71df.jpg',
              title:'西安钟楼',
              desc:'位于陕西省西安市...'
             },
              {
              id:'003',
              imgUrl:'http://img1.qunarzz.com/sight/p0/1704/a3/a3e4f87ebd5c55a1a3.water.jpg_200x200_f1fc0289.jpg',
              title:'西安幻太奇梦幻海洋馆',
              desc:'西安幻太奇梦幻海洋馆...'
             },
          ]
      }
  }
}
</script>

<style lang="scss" scoped>
    @import '~styles/varibles.scss';
   .tlitle{
       margin-top: .2rem;
       line-height: .8rem;
       background: #eee;
       text-indent: .2rem;
   }
   .item{
       display: flex;
       height: 1.9rem;
       overflow: hidden;
       .item-img-wrapper{
         margin-left: .1rem;
         display: flex;
         align-items: center;
         justify-content: center;
         .item-img{
           width: 1.7rem;
           height: 1.4rem;
           padding: .1rem;
         }
       }
       
       .item-info{
           flex: 1;
           padding: .1rem;
           min-width: 0;
           .item-title{
               line-height: .54rem;
               font-size: .32rem;
               @include ellipsis()
           }
           .item-desc{
               line-height: .4rem;
               color: #ccc;
               @include ellipsis()
           }
           .item-button{
               line-height: .44rem;
               background: #ff9300;
               padding: 0 .2rem;
               border-radius: .06rem;
               margin-top: .2rem;
               color: #fff;
           }
       }
   }
</style>
