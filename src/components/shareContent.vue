<template>
  <div class='content'>

    <h1 class="service_title">服务流程</h1>
    <div class='banner'>
      <img :src='src'/>
    </div>
    <h1 class="service_title">解决方案</h1>
    <div class='introduce'>
      <div class='pic mar1'>
        <img :src='src2'/>
        <div class='ad'>
          <h3>云计算</h3>
          <p class='word'>文案待写</p>
          <p class='word'></p>
        </div>
      </div>
    </div>
    <div class='introduce'>
      <div class='pic mar1'>
        <img :src='src2'/>
        <div class='ad'>
          <h3>移动app</h3>
          <p class='word'>文案待写</p>
          <p class='word'></p>
        </div>
      </div>
    </div>
    <div class='introduce'>
      <div class='pic mar1'>
        <img :src='src4'/>
        <div class='ad'>
          <h3>小程序</h3>
          <p class='word'>文案待写</p>
          <p class='word'></p>
        </div>
      </div>
    </div>
    <div class='introduce'>
      <div class='pic mar1'>
        <img :src='src2'/>
        <div class='ad'>
          <h3>web网站</h3>
          <p class='word'>文案待写</p>
          <p class='word'></p>
        </div>
      </div>
    </div>

  </div>
</template>
<script>
  export default {
    name: 'shareContent',
    data() {
      return {
        src: '/static/img/serice.jpg',
        src2: '/static/img/service_yun.jpg',
        src2: '/static/img/service_yun.jpg',
        src4: '/static/img/small_wechat.jpg'

      }
    }
  }
</script>
<style lang='scss'>
  @mixin fade-in {
    -webkit-animation: fadeIn 2s 0.5s ease both;
    -moz-animation: fadeIn 2s 0.5s ease both;
    -ms-animation: fadeIn 2s 0.5s ease both;
    -o-animation: fadeIn 2s 0.5s ease both;
    animation: fadeIn 2s 0.5s ease both;
  }

  .service_title {
    margin-top: 30px;
    margin-bottom: 0px;
  }

  .introduce {
    position: relative;
    width: 100%;
    height: 100%;
    top: -10%;

    img {
      width: 400px;
      height: 400px;
    }
  }

  .pic {
    position: relative;

    img {
      left: -15%;
      position: relative;
    }
  }

  .ad {
    position: absolute;
    top: 10%;
    left: 55%;
    width: 336px;

    h3 {
      text-align: left;
      font-size: 36px;
      color: #585858;
      font-weight: 500;
    }
  }

  .word {
    font-size: 14px;
    color: #4b4b4b;
    line-height: 22px;
    text-align: left;
    margin: 0;
    padding: 0;
    padding-bottom: 10px;
  }

  .mar1 {
    margin: 50px 0 50px;
  }
</style>
