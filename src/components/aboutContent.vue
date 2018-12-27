<template>
	<div class='content'>
		<div class='banner'>
			<h3 id='about'>ofo 共享单车首创“单车共享”模式<br>是全球第一个无桩共享单车平台</h3>
			<img :src='src' />
		</div>
		<div>
			<div class='mar' v-for='item in docs'>
				<h3>{{item.h3}}</h3>
				<p class='word'>{{item.p1}}</p>
				<p class='word'>{{item.p2}}</p>
				<p class='word'>{{item.p3}}</p>
				<p class='word'>{{item.p4}}</p>
			</div>
		</div>
	</div>
</template>
<script>
	const docs = [{
		h3: '我们是谁？',
		p1: '深圳市小鹿科技有限公司成立于2019年1月1日，主要成员来自腾讯、华为、360等一线互联网公司',
		p2: '资深工程师，高效，低成本，丰富软件系统开发经验',
		p3: '',
		p4: ''
	},{
		h3: '我们要干什么？',
		p1: '致力于为合作伙伴定制云计算、大数据、APP、区块链应用解决方案，助力客户提升产品和服务竞争力',
		p2: '客户提供成熟可靠的APP、DAPP、Web、小程序解决方案',
		p3: '',
		p4: ''
	},{
		h3: '未来，愿景',
		p1: '深圳市小鹿科技将成为一流的企业级方案公司，助力传统企业转型互联网',
		p2: '',
		p3: '',
		p4: ''
	}];
	export default {
		name: 'shareContent',
		data () {
			return {
				src: '/static/img/about.jpg',
				docs: docs
			}
		}
	}
</script>
<style lang='scss'>
	#about{
		text-align: left;
		position: absolute;
		top: 16%;
		left: 20%;
		z-index: 8;
		color: white;
		font-size: 34px;
        line-height: 130%;
        animation: fadeIn 2s 0.5s ease both;
	}
	.mar{
		margin: 50px 0 50px;
		h3 {
			font-size: 36px;
			padding: 42px 0 26px;
			font-weight: 500;
			color: #666;
		}
		p {
			line-height: 32px;
			font-size: 14px;
			color: #8d8d8d;
			text-align: center;
		}
	}
</style>
