<template>
  <div class="list" ref="wrapper">
    <div>
        <div class="area">
          <div class="title border-topbottom">当前城市</div>
          <div class="button-list">
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
          </div>
        </div>
          <div class="area">
          <div class="title border-topbottom">热门城市</div>
            <div class="button-list">
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
          </div>
        </div>
        <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
         <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
         <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
         <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
         <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
         <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
            <div class="item border-bottom">阿里尔</div>
          </div>
        </div>
      </div>  
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: "CityList",
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
};
</script>

<style lang="scss" scoped>
@import "~styles/varibles.scss";
.list {
  position: absolute;
  overflow: hidden;
  top: 1.58rem;
  left: 0;
  right: 0;
  bottom: 0;
  // background: #666;
  .area {
    .title {
      line-height: 0.6rem;
      font-style: 0.26rem;
      background: #eee;
      padding-left: 0.2rem;
      color: #666;
    }
    .border-topbottom {
      &::before,
      &::after {
        border-color: #ccc;
      }
    }
    .button-list {
      padding: 0.1rem 0.6rem 0.1rem 0.1rem;
      overflow: hidden;
      .button-wrapper {
        float: left;
        width: 33.33%;
        .button {
          padding: 0.1rem;
          margin: 0.1rem;
          text-align: center;
          border: 0.02rem solid #ccc;
          border-radius: 0.06rem;
        }
      }
    }
   .item-list{
     .item{
       line-height: .76rem;
       color: #666;
       padding-left: .2rem;
     }
     .border-bottom{
       &::before{
         border-color: #ccc;
       }
     }
   } 
  }
}
</style>


