<template>
    <footer>
        <div class='address'>
            <div class='data'>
                <img :src='src' />
                <p>281421465@qq.com（周一至周日：7:00 - 24:00）</p>
                <p>深圳市南山区科兴科技园A座1409</p>
            </div>
            <div class='link'>
                <a id='github' href='https://github.com/jiangyuanyuan' target='_blank'/>
                <a id='wechat' href='javascript:;' @mouseover='show' @mouseleave='hide'/>
            </div>
        </div>
        <div class='company'>
            <p>Copyright © 2017 beer-smart Inc. 保留所有权利。  商务合作邮箱  281421465@qq.com</p>
        </div>
    </footer>
</template>

<script>

export default {
    name: 'header',
    data () {
        return {
            src: '/static/img/logo.png'
        }
    },
    methods: {
        show () {
            this.src = '/static/img/wx-qrcode.png';
        },
        hide () {
            this.src = '/static/img/logo.png';
        }
    }
}
</script>

<style lang='scss'>
    footer{
        top: 1000px;
        margin-top: 10px;
        left: 0;
        height: 310px;
        background: #191919;
    }
    .address {
        height: 251px;
        font-size: 12px;
        color: #a3a3a3;
        text-align: center;
    }
    .company {
        border-top: 1px solid #2b2b2b;
        font-size: 12px;
        color: #a3a3a3;
        text-align: center;
    }
    .address img{
        width: 75px;
        height: 72px;
    }
    .data{
        position: relative;
        top: 20%;
    }
    .link{
        font-size: 12px;
        color: #a3a3a3;
        text-align: center;
        position: relative;
        top: 25%;
    }
    @mixin img-style{
        display: inline-block;
        width: 24px;
        height: 22px;
    }
    #github {
        background: url('/static/img/github.png');
        @include img-style;
        margin-right: 35px;
    }
    #wechat {
        background: url('/static/img/social_icon.png');
        @include img-style;
        background-position: -24px 0;
    }
</style>
