<!-- 组件的模板 -->
<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <!-- banner -->
                    <div v-swiper:mySwiper="swiperOption" class="banner">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide" v-for="banner in banners">
                                <img :src=banner>
                            </div>
                        </div>
                        <div class="swiper-pagination swiper-pagination-white"></div>
                        <div class="swiper-button-prev swiper-button-white"></div>
                        <div class="swiper-button-next swiper-button-white"></div>
                    </div>
                    <!-- 推荐专题 -->
                    <div class="recommend-collection">
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.jpg" alt="">
                            <span>读书</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>故事</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection1.jpg" alt="">
                            <span>摄影</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>手绘</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection2.jpg" alt="">
                            <span>旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/collection/123">
                            <img src="../assets/img/collection3.jpg" alt="">
                            <span>@IT·互联网</span>
                        </nuxt-link>
                        <nuxt-link class="more-hot-collection" to="/collection/123">
                            更多热门专题
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!-- 文章列表 -->
                    <div id="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/logo.png">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同， 于是市场上出现很多读书方法，比如速度、多读、慢读、列读…… 不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短篇小说
                                        </nuxt-link>
                                        <nuxt-link class="" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/logo.png">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同， 于是市场上出现很多读书方法，比如速度、多读、慢读、列读…… 不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短篇小说
                                        </nuxt-link>
                                        <nuxt-link class="" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/logo.png">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同， 于是市场上出现很多读书方法，比如速度、多读、慢读、列读…… 不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短篇小说
                                        </nuxt-link>
                                        <nuxt-link class="" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/logo.png">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同， 于是市场上出现很多读书方法，比如速度、多读、慢读、列读…… 不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            短篇小说
                                        </nuxt-link>
                                        <nuxt-link class="" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <!-- 阅读更多 -->
                    <nuxt-link to="" class="load-more">
                        阅读更多
                    </nuxt-link>
                </div>
                <div class="col-4 aside">
                    <div class="board">
                        <nuxt-link to="/">
                            <img src="../assets/img/新上榜.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/七日热门.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/30日热门.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/简书出版.png" alt="">
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/简书大学堂.png" alt="">
                        </nuxt-link>
                    </div>
                    <nuxt-link to="/" class="download">
                        
                    </nuxt-link>
                    <div class="recommend-author">
                        <div class="title">
                            <span>推荐作者</span>
                            <a href="javascript:void(0)" class="page-change" @click="rotate">
                                <i class="fa fa-refresh" ref="refresh"></i>
                                换一批
                            </a>
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/logo.png" alt="">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/logo.png" alt="">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/logo.png" alt="">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/logo.png" alt="">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k字·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link to="/u/123" class="avatar">
                                    <img src="../assets/img/logo.png" alt="">
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="follow">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link to="/u/123" class="name">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k字·7.2k喜欢
                                </p>
                            </li>
                        </ul>
                        <nuxt-link to="/" class="find-more">
                            查看全部
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <footer class="my-container">
            <div class="row">
                <div class="row-12 main">
                    <nuxt-link to="/p/123" class="a">
                        关于简书
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        联系我们
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        加入我们
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        简书出版
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        品牌与徽标
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        帮助中心
                    </nuxt-link>
                    ·
                    <nuxt-link to="/p/123" class="a">
                        合作伙伴
                    </nuxt-link>
                    <p>
                        ©2012-2018 上海佰集信息科技有限公司 / 简书 / 沪ICP备11018329号-5 / Smrz 沪公网安备31010402002252号 / Wxb 举报电话：021-34770013 / Zggsrz
                    </p>
                </div>
            </div>
        </footer>
    </div>
</template>

<!-- 组件的模型 -->
<script>
    import myHeader from '../components/myHeader.vue'
    export default {
        data() {
            return {
                banners: ['/banner1.jpg', '/banner2.jpg', '/banner3.jpg', '/banner4.jpg'],
                swiperOption: {
                    autoplay: {
                        delay: 3000,//切换时间
                        stopOnLastSlide: false,//是否停止在最后一张
                        disableOnInteraction: false,//禁止轮播
                    },
                    pagination: {
                        el: '.swiper-pagination'
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                }
            }
        },
        components: {
            myHeader
        },
        mounted() {

        },
        methods: {
            rotate: function () {
                this.deg = this.deg + 360;
                this.$refs.refresh.style.transform = `rotate(${this.deg}deg)`;
            }
        }
    }
</script>
<style>
</style>