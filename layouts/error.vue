<template>
  <section class="container">
    <nuxt-link to="/">
      <img class="a" src="../assets/img/404-1.png" alt="">
    </nuxt-link>
    <div class="b">
      <div class="b-1">
        <img src="../assets/img/404-2.png" alt="">
        <h3>您要找的页面不存在</h3>
        <span>可能是因为您的链接地址有误、该文章已经被作者删除或转为私密状态。</span>
        <nuxt-link class="active" to="/">返回「简书」首页</nuxt-link>
      </div>
    </div>
    <div class="c">
      <div class="c-1">
        <div class="c-1-1">
          <img src="../assets/img/404-3.png" alt="">
        </div>
        <div class="c-1-2">
          <span>免费下载简书手机app ›</span>
          <p>创作你的创作</p>
        </div>
      </div>
      <div class="c-1">
        <div class="c-1-1">
          <img src="../assets/img/404-4.png" alt="">
        </div>
        <div class="c-1-2">
          <span>关注简书官方微博 ›</span>
          <p>看看大家的精彩创作</p>
        </div>
      </div>
      <div class="c-1 dd">
        <div class="c-1-1">
          <img src="../assets/img/404-5.png" alt="">
        </div>
        <div class="c-1-2">
          <span>关注简书官方微信</span>
          <p>每天为你推送精选文章</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
  export default {
    props: ['error']
  }
</script>

<style scoped>
@media (max-width:768px){
    .a{
        display: none;
    }
}
  .a {
    position: absolute;
    left: 40px;
    top: 40px;
    width: 300px;
    cursor: pointer;
  }

  .b {
    width: 100%;
    max-width: 1440px;
    margin: 0 auto;
    text-align: center;
  }

  .b .b-1 {
    padding-top: 80px;
    padding-bottom: 20px;
    display: block;
  }

  .b .b-1 img {
    width: 220px;
  }

  .b .b-1 h3 {
    margin: 40px 0 20px 0;
    font-weight: bold;
    display: block;
    font-size: 20px;
    ;
  }

  .b .b-1 span {
    margin: 10px 0 30px 0;
    font-size: 14px;
    display: block;
  }

  .b .b-1 .active {
    padding: 13px 0;
    width: 160px;
    font-size: 15px;
    border-radius: 40px;
    color: #ffffff!important;
    background-color: #42C02E;
    border-color: #42C02E;
    display: inline-block;
  }

  .c {
    margin-top: 40px;
    border-top: 1px solid #F0F0F0;
    display: block;
    text-align: center;
  }

  .c .c-1 {
    float: left;
    width: 33%;
    padding: 30px 0;
    border-right: 1px solid #F0F0F0;
  }
  .c .dd{
    border-right: none;
  }
  .c .c-1 .c-1-1 {
    display: inline-block;
  }

  .c .c-1 .c-1-1 img {
    height: 60px;
    margin-right: 15px;
    vertical-align: middle;
  }

  .c .c-1 .c-1-2 {
    font-size: 14px;
    padding-top: 10px;
    text-align: left;
    display: inline-block;
    vertical-align: middle;
  }

  .c .c-1 .c-1-2 span {
    color: #333333;
    cursor: pointer;
    text-decoration: none;
  }

  .c .c-1 .c-1-2 p {
    font-size: 12px;
    color: #9B9B9B;
    margin-top: 10px;
  }
</style>