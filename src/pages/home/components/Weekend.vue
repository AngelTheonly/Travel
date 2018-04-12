<template>
  <div>
    <div class="tlitle"> 周末去哪 </div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
      return{
          recommendList:[
              {
              id:'001',
              imgUrl:'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
              title:'秦始皇陵博物院（兵马俑）',
              desc:'位于陕西省西安市临潼处...'
             },
              {
              id:'002',
              imgUrl:'http://img1.qunarzz.com/sight/source/1505/30/67d5e62ca78a29.jpg_r_640x214_9dfb4295.jpg',
              title:'西安花花世界',
              desc:'月落星驰又一春，不负人间看花人...'
             },
              {
              id:'003',
              imgUrl:'http://img1.qunarzz.com/sight/source/1511/14/1cf5dc2ecbfc16.jpg_r_640x214_b4b3a58a.jpg',
              title:'最美丝路行',
              desc:'情系西北，中国梦丝路行...'
             },
          ]
      }
  }
}
</script>

<style lang="scss" scoped>
    @import '~styles/varibles.scss';
   .tlitle{
       line-height: .8rem;
       background: #eee;
       text-indent: .2rem;
   }
   .item{
      
       .item-img-wrapper{
         height: 0;
         overflow: hidden;
         padding-bottom: 33.9%;
         .item-img{
           width: 100%;
         }
       }
       
       .item-info{
           padding:0.1rem 0.2rem;
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
       }
   }
</style>
