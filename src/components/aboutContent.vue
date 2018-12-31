<template>
	<div class='content'>
		<div class='banner'>
      <h2 id='about'>走在梦想的路上，总是那么有趣</h2>
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
    <h1>加入我们</h1>
    <div class='jobEmail'>
      <div class='jobContainer'>
        <div class='jobList' v-for='item in jobdocs'>
          <h3>{{item.title}}</h3>
          <p>{{item.data1}}</p>
          <p>{{item.data2}}</p>
          <p>{{item.data3}}</p>
        </div>
      </div>
      <div class='email'>
        <div>更多职位</div>
        <p>联系方式：281421465@qq.com</p>
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
  const jobdocs = [{
    title: '产品设计',
    data1: '产品经理',
    data2: 'UI设计师'
  },{
    title: '技术研发',
    data1: '后端工程师',
    data2: '前端工程师',
    data3: '移动端工程师'

  },{
    title: '市场运营',
    data1: '客户经理',
    data2: '销售代表'
  }];
	export default {
		name: 'shareContent',
		data () {
			return {
				src: '/static/img/share1.jpg',
				docs: docs,
        jobdocs:jobdocs
			}
		}
	}
</script>
<style lang='scss'>
	#about{
		text-align: left;
		position: absolute;
		top: 56%;
    left: 25%;
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
  .jobContainer {
    display: flex;
    justify-content: space-around;
  }
  .jobEmail {
    margin: 60px 0 100px;
    p {
      display: block;
      height: 24px;
      line-height: 24px;
      color: #b8b8b8;
      font-size: 14px;
      margin: 0;
      padding: 0;
      cursor: pointer;
    }
  }
  .email {
    margin-top: 40px;
    div {
      width: 134px;
      height: 58px;
      line-height: 58px;
      display: block;
      margin: 0 auto;
      text-align: center;
      border: 1px solid #e5e5e5;
      font-size: 14px;
      color: #333333;
      border-radius: 30px;
      cursor: pointer;
      &:hover {
        background-color: #ffc107;
      };
      + p {
        margin-top: 40px;
        cursor: auto;
      }
    }
  }
  .jobList {
    width:100%;
    h3 {
      font-size: 18px;
      text-align: center;
      color: #585858;
      margin-bottom: 16px;
    }
    p {
      &:hover{
        color:#585858;
      }
    }
  }
</style>
