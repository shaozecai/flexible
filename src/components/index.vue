<template>
     <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img1.jpg" alt="">
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img2.jpg" alt="">
          <div class="text text1">
            <ul>
              <li class="title"><font>第一回</font>  投师名门</li>
              <li>你看这些<font>白云</font> ，聚了又聚 ，</li>
              <li>散了又散 。人生<font>离合</font> ，</li>
              <li><font>复亦如斯 。</font></li>
              <li>你又何必烦恼 ？</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img3.jpg" alt="">
          <div class="text text2">
            <ul>
              <li class="title"><font>第二回</font>  出入武林</li>
              <li><font>生死有命</font> ，人身无常 ，</li>
              <li><font>因缘离合 ，</font>岂能强求 ？</li>
              <li><font>过儿</font> ， 忧能伤人 ，</li>
              <li>你别太过<font>关怀</font>了 。</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img4.jpg" alt="">
          <div class="text text3">
            <ul>
              <li class="title"><font>第三回</font>  修炼武功</li>
              <li>孩儿 ，<font>你长大了之后</font> ，</li>
              <li>要提防<font>女人</font>骗你 ，</li>
              <li>越是<font>好看</font>的女人</li>
              <li>越会骗人 。</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img5.jpg" alt="">
          <div class="text text4">
            <ul>
              <li class="title"><font>第四回</font>  传授武艺</li>
              <li>石头啊<font>石头</font> ，</li>
              <li>你<font>寂寞</font>了多年 ，</li>
              <li><font>今日</font>令狐冲又来</li>
              <li><font>和你相伴</font>了 。</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img  class="swiper-lazy" src="../assets/images/img6.jpg" alt="">
          <div class="text text5">
            <ul>
              <li class="title"><font>第五回</font>  笔试答题</li>
              <li><font>王姑娘</font> ，</li>
              <li>这<font>一生一世</font> ，</li>
              <li>我是<font>永远</font>也不会</li>
              <li>对你生气的。</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="box">
          <img class="swiper-lazy" src="../assets/images/img7.jpg" alt="">
          <div class="text text6">
            <ul>
              <li class="title"><font>第六回</font>  武林秘籍</li>
              <li>我是江湖上人称<font>水上小白龙</font></li>
              <li>能够连续<font>三天三夜</font></li>
              <li><font>在水中气都不喘</font> ，生食鱼虾蟹</li>
              <li>都面不改色的<font>小白龙韦小宝</font>。</li>
            </ul>
          </div>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
      <!-- <div class="swiper-button-prev" slot="button-prev"></div> -->
      <div class="swiper-button-next" slot="button-next"></div>
      <!-- <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
    </swiper>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    var that = this;
    return {
      msg: 'Welcome to Your Vue.js App',
      swiperOption: {
        direction: 'vertical',
        loop:true,
        width: window.innerWidth,
        height: window.innerHeight,
        observer:true,
        grabCursor: true,
        pagination: {
          el: '.swiper-pagination',
          type: 'bullets',
          clickable: true,
        },
        navigation: {
          nextEl: '.swiper-button-next'
        },
        //窗口缩放时设置width
        on: {
          resize: function(){
            this.params.width = window.innerWidth;
            this.params.height = window.innerHeight;
            this.update();
          },
        } ,

      }

    }
  },
  methods:{
   
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper
    }
  },
  mounted() {      
    //this.swiper.slideTo(3, 1000, false)
  }


}
</script>

<style  scoped>
  *{
    margin: 0;
    padding: 0;
  }
  h2{
    font-size: 50px;
  }
  img{
    display: block;
    width: 100%;
    height: 100%;
    position: absolute;
  }
  .box{
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
  }
   html, body {
      position: relative;
      height: 100%;
    }
    body {
      background: #eee;
      font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
      font-size: 14px;
      color:#000;
      margin: 0;
      padding: 0;
    }
    .swiper-container {
      width: 100%;
      height: 100%;
    }
    .swiper-slide {
      text-align: center;
      font-size: 30px;
      background: #fff;
      display: -webkit-box;
      display: -ms-flexbox;
      display: -webkit-flex;
      display: flex;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-box-align: center;
      -ms-flex-align: center;
      -webkit-align-items: center;
      align-items: center;
    }
   
    .swiper-container-vertical > .swiper-pagination-bullets{
      top:50vh;
    }
    .swiper-button-prev, .swiper-button-next{
      top:92vh;
      right: 50%;
      transform: rotate(90deg);
      outline: none;
      background-image:url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M27%2C22L27%2C22L5%2C44l-2.1-2.1L22.8%2C22L2.9%2C2.1L5%2C0L27%2C22L27%2C22z'%20fill%3D'%23ffffff'%2F%3E%3C%2Fsvg%3E")
    }
    .text{
      position: absolute;
      top:6%;
      left: 10%;
      background: rgba(255, 255, 255, .8);
      padding: 25px;
    }
    .text2{
      top:570px;
      left:180px;
    }
    .text3{
      top:170px;
      left:180px;
    }
    .text4{
      top:170px;
      left:60px;
    }
    .text5{
      top:20px;
      left:98px;
    }
    .text6{
      top:220px;
      left:200px;
    }
    li{
      list-style: none;
      width: 30px;
      font-size: 26px;
      float: left;
      word-break: break-all;
      padding: 28px;
      line-height: 1.2;
      border-top: 1px solid #dedede;
      border-left: 1px solid #dedede;
      border-bottom: 1px solid #dedede;
    }
    .title{
      width: 40px;
      font-size: 30px;
      font-weight: bold;
      line-height: 1.4;
      padding: 24px;
    }
    font{
      color: #ba1212;
    }
    .title font{
      display: inline-block;
      padding-bottom: 26px;
      color: #333;
    }
</style>
