<template>
  <div >
    <h1 id='info'>云计算 大数据 移动应用 小程序</h1>
    <div class="swipe">
      <swiper :options="swiperOption" >
        <swiper-slide v-for="item in imgArr" :key='item.src'><img :src="item.src"/></swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>

</template>

<script>
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	const imgArr = [{
		src:'/static/img/share1.jpg'
	}];
	export default {
		name: 'swipe',
		components: {
			swiper,
			swiperSlide
		},
		data() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					paginationClickable: true,
                    autoplay: 5000

				},
				imgArr: imgArr
			}
		}
  }
</script>

<style>
  #info{
    text-align: left;
    position: absolute;
    top: 40%;
    left: 20%;
    right: 15%;
    z-index: 8;
    color: white;
    font-size: 60px;
    line-height: 130%;
    animation: fadeIn 2s 0.5s ease both;
  }
	.swipe {
		left: 0;
		top: 0;
		width: 100%;
		margin: 0;
		padding: 0;
	}
    img {
		width:100%;
		height:100%;
        left: 0px;
    }
</style>
