<template>
    <div>
        <my-header></my-header>
        <div class="container person">
            <div class="row">
                <div class="col-xs-16 main">
                    <div class="main-top">
                        <a class="avatar" href="#">
                            <img src="//upload.jianshu.io/users/upload_avatars/9093889/b85fcb0f-244c-4a3d-8872-5d709936c98d?imageMogr2/auto-orient/strip|imageView2/1/w/240/h/240"
                                alt="240">
                        </a>

                        <div class="title">
                            <a class="name" href="#">超凡_bd85</a>
                            <i class="fa fa-mars"></i>
                        </div>
                        <div class="info">
                            <ul>
                                <li>
                                    <div class="meta-block">
                                        <a href="#">
                                            <p>0</p>
                                            关注
                                            <i class="fa fa-angle-right"></i>
                                        </a>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <a href="#">
                                            <p>1</p>
                                            粉丝
                                            <i class="fa fa-angle-right"></i>
                                        </a>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <a href="#">
                                            <p>0</p>
                                            文章
                                            <i class="fa fa-angle-right"></i>
                                        </a>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <p>0</p>
                                        <div>字数</div>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <p>0</p>
                                        <div>收获喜欢</div>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div id="outer-container">
                        <ul class="trigger-menu" data-pjax-container="#list-container">
                            <li class="">
                                <nuxt-link to="guanzhudezhuanti">
                                    关注的专题/文集/连载 0
                                </nuxt-link>
                            </li>
                            <li class="active">
                                <nuxt-link to="xihuandewenzhang">
                                    喜欢的文章 1
                                </nuxt-link>
                            </li>
                        </ul>

                        <div id="list-container">
                            <!-- 动态列表模块 -->
                            <ul class="note-list" infinite-scroll-url="/users/9a6682699277/timeline">

                                <!-- 喜欢了文章 -->
                                <li class="have-img" id="feed-258429613">
                                    <a class="wrap-img" href="#">
                                        <img src="//upload-images.jianshu.io/upload_images/8475271-aabc90931a25251b.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/150/h/120"
                                            alt="120">
                                    </a>
                                    <div class="content">
                                        <div class="author">
                                            <a class="avatar" href="#">
                                                <img src="//upload.jianshu.io/users/upload_avatars/9093889/b85fcb0f-244c-4a3d-8872-5d709936c98d?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180"
                                                    alt="180">
                                            </a>
                                            <div class="info">
                                                <a class="nickname" href="#">超凡_bd85</a>
                                                <span data-type="like_note" data-datetime="2018-02-17T18:14:38+08:00"> 喜欢了文章 · 02.17 18:14</span>
                                            </div>
                                        </div>

                                        <nuxt-link class="title" to="/p/123">汪洋中的一条船</nuxt-link>

                                        <p class="abstract">午夜，一部老电影伴我无眠 我为郑丰喜的命运纠结 丰富的感情跌宕着汪洋中的一条船 风雨中那个跪着赶鸭子的孩子 扣动着我的心弦 伟大的人都是努力“努”出来的 振奋人心的话语让自己...</p>

                                        <div class="meta">
                                            <div class="origin-author">
                                                <a href="#">独秀一栀</a>
                                            </div>
                                            <nuxt-link to="/p/123">
                                                <i class="fa fa-eye"></i> 336
                                            </nuxt-link>
                                            <nuxt-link to="/p/123">
                                                <i class="fa fa-comment"></i> 73
                                            </nuxt-link>
                                            <span>
                                                <i class="fa fa-heart"></i> 87</span>
                                        </div>
                                    </div>
                                </li>
                            </ul>
                        </div>
                        
                    </div>
                </div>

                <div class="col-xs-7 col-xs-offset-1 aside">
                    <div class="description">
                        <div class="js-intro"></div>


                    </div>
                    <div id="user-publications">
                        <!---->
                    </div>
                    <div id="user-courses">
                        <!---->
                    </div>
                    <ul class="list user-dynamic">
                        <li>
                            <a href="#">
                                <i class="fa fa-th-large"></i>
                                <span>我关注的专题/文集/连载</span>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa fa-heart-o"></i>
                                <span>我喜欢的文章</span>
                            </a>
                        </li>
                    </ul>
                    <!-- 专题和文集 -->
                    <div>
                        <div>
                            <!---->
                            <div class="title">我创建的专题</div>
                            <div class="new-collection-block">
                                <a href="#" class="new-collection-btn">
                                    <i class="fa fa-plus"></i>
                                    <span>创建一个新专题</span>
                                </a>
                            </div>
                        </div>
                        <!---->
                        <!---->
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../../../components/myHeader'
    export default {
        data() {
            return {

            }
        },
        components: {
            myHeader
        }
    }
</script>
<style scoped>
    @media (min-width: 992px) {
        .container {
            width: 960px;
        }
    }

    @media (min-width: 1081px) {
        .container {
            width: 960px;
        }
    }

    @media (min-width: 992px) {
        .container {
            width: 970px;
        }
    }

    /* @media (min-width: 768px) {
        .container {
            width: 750px;
        }
    } */

    .person .row {
        padding-top: 30px;
    }

    .row {
        margin-left: -15px;
        margin-right: -15px;
    }

    .row:after {
        clear: both;
    }

    .row:after,
    .row:before {
        content: " ";
        display: table;
    }

    *,
    :after,
    :before {
        box-sizing: border-box;
    }

    .person .main {
        padding-right: 0;
    }

    .col-xs-16 {
        width: 66.66667%;
        float: left;
        position: relative;
        min-height: 1px;
        padding-left: 15px;
    }

    .person .main .main-top {
        margin-bottom: 20px;
    }

    .person .main .main-top .avatar {
        float: left;
        width: 80px;
        height: 80px;
        margin-left: -2px;
    }

    .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 50%;
    }

    img {
        vertical-align: middle;
    }

    .person .main .main-top .title {
        padding: 5px 0 0 100px;
    }

    .person .main .main-top .title .name {
        display: inline;
        font-size: 21px;
        font-weight: 700;
        vertical-align: middle;
    }

    .person .main .main-top .fa-mars {
        font-size: 16px;
        vertical-align: middle;
        margin-left: 5px;
        margin-top: 5px;
    }

    .fa-mars {
        color: #3194d0;
    }

    .person .main .main-top .info {
        margin-top: 5px;
        padding-left: 100px;
        font-size: 14px;
    }

    .person .main .main-top .info ul {
        font-size: 0;
    }

    .person .main .main-top .info ul li {
        display: inline-block;
    }

    li {
        line-height: 20px;
    }

    .person .main .main-top .info ul .meta-block {
        font-size: 12px;
        margin: 0 7px 6px 0;
        padding: 0 7px 0 0;
        border-right: 1px solid #f0f0f0;
    }

    .person .main .main-top .info ul div {
        color: #969696;
    }

    .person .main .main-top .info ul a {
        color: #969696;
    }

    .person .main .main-top .info ul p {
        margin-bottom: -3px;
        font-size: 15px;
        color: #333;
    }

    p {
        margin: 0 0 10px;
    }

    .person .main .main-top .info ul .meta-block .ic-arrow {
        margin-left: -3px;
    }

    .trigger-menu {
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        font-size: 0;
        list-style: none;
    }

    .trigger-menu li {
        position: relative;
        display: inline-block;
        padding: 8px 0;
        margin-bottom: -1px;
    }

    .trigger-menu a {
        padding: 13px 20px;
        font-size: 15px;
        font-weight: 700;
        color: #969696;
        line-height: 25px;
    }

   .trigger-menu li::after {
        content: "";
        position: absolute;
        left: 50%;
        top: 100%;
        bottom: 0px;
        width: 0;
        transition: all ease 0.3s;
        opacity: 0;
        border-bottom: 2px solid #646464;
    }

    .trigger-menu li:hover {
        color: #646464!important;
    }

    .trigger-menu li:hover::after {
        left: 0%;
        width: 100%;
        opacity: 1;
        border-bottom: 2px solid #646464;
    }

    .trigger-menu i {
        margin-right: 5px;
        font-size: 17px;
    }

    .trigger-menu li.active {
        border-bottom: 2px solid #646464;
    }

    .note-list li {
        position: relative;
        width: 100%;
        margin: 0 0 17px;
        padding: 0 2px 17px 0;
        border-bottom: 1px solid #f0f0f0;
        word-wrap: break-word;
    }

    .note-list .have-img .wrap-img {
        position: absolute;
        top: 50%;
        margin-top: -68px;
        right: 0;
        width: 150px;
        height: 120px;
    }

    .note-list .author a {
        color: #333;
    }

    .avatar {
        width: 32px;
        height: 32px;
        display: block;
        cursor: pointer;
    }

    .note-list .author .info .nickname {
        vertical-align: middle;
    }

    .note-list .author .info span {
        display: inline-block;
        padding-left: 3px;
        color: #969696;
        vertical-align: middle;
    }

    .note-list .title {
        margin: -7px 0 4px;
        display: inherit;
        font-size: 18px;
        font-weight: 700;
        line-height: 1.5;
    }

    .note-list .origin-author {
        display: inline;
        margin-bottom: 5px;
        font-size: 12px;
        color: #969696;
    }

    .person .aside {
        padding: 0;
    }

    .col-xs-offset-1 {
        margin-left: 4.16667%;
    }

    .col-xs-7 {
        width: 29.16667%;
        float: left;
        position: relative;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
    }

    .person .aside .description {
        position: relative;
        margin-bottom: 16px;
        padding: 0 0 16px;
        text-align: left;
        font-size: 0;
        border-bottom: 1px solid #f0f0f0;
        clear: both;
        word-break: break-word!important;
        word-break: break-all;
    }

    .person .aside .description .js-intro {
        margin-bottom: 10px;
        line-height: 20px;
        font-size: 14px;
    }

    #user-publications {
        box-sizing: border-box;
    }

    #user-courses {
        box-sizing: border-box;
    }

    .person .aside .user-dynamic {
        padding-bottom: 6px;
    }

    .person .aside .list {
        margin-bottom: 16px;
        padding-bottom: 16px;
        list-style: none;
        border-bottom: 1px solid #f0f0f0;
        clear: both;
    }

    .person .aside .list li {
        margin-bottom: 10px;
    }

    .person .aside .list li a {
        display: inline-block;
    }

    .person .aside .user-dynamic a {
        font-size: 14px;
        color: #333;
        line-height: 30px;
    }

    .person .aside a,
    .person .aside a:hover {
        color: #3194d0;
    }

    .person .aside .user-dynamic i {
        margin-right: 10px;
        font-size: 20px;
        vertical-align: middle;
    }

    .person .aside .user-dynamic span {
        vertical-align: middle;
    }

    .person .aside .title {
        float: left;
        margin-bottom: 10px;
        font-size: 14px;
        color: #969696;
    }

    .person .aside .new-collection-block {
        position: relative;
        margin-bottom: 16px;
        padding: 0 0 16px;
        text-align: left;
        font-size: 0;
        border-bottom: 1px solid #f0f0f0;
        clear: both;
        word-break: break-word!important;
        word-break: break-all;
    }

    .person .aside .new-collection-block a {
        margin-right: 5px;
    }

    .person .aside .new-collection-btn i {
        font-size: 13px;
        color: #42c02e;
        padding-right: 2px;
    }

    .person .aside .new-collection-btn span {
        font-size: 13px;
        color: #42c02e;
    }
</style>