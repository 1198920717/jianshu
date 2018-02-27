<template>
    <div>

        <div id="list-container">
            <!-- 动态列表模块 -->
            <ul class="note-list">
                <!-- 喜欢了文章 -->
                <li class="have-img" id="feed-258429613">
                    <a class="wrap-img" href="#">
                        <img src="//upload-images.jianshu.io/upload_images/8475271-aabc90931a25251b.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/150/h/120"
                            alt="120">
                    </a>
                    <div class="content">
                        <div class="author">
                            <a class="avatar" href="#">
                                <img src="../../../assets/img/头像.jpg"
                                    alt="180">
                            </a>
                            <div class="info">
                                <a class="nickname" href="#">超凡</a>
                                <span data-type="like_note" data-datetime="2018-02-17T18:14:38+08:00"> 喜欢了文章 · 02.17 18:14</span>
                            </div>
                        </div>

                        <nuxt-link class="title" to="/p/123">我又要不自量力的谈一谈关于简书的话题了</nuxt-link>

                        <p class="abstract">简书的定位究竟是怎样的呢？这个正确答案在简书高层的内心深处，普通员工都不一定清晰，我们吃瓜群众来谈它的定位，那就只能是“玄之又玄”了，无根无据，纯属猜测，所以大家首先要调整一下心态，对以下文字和观点放低一下要求哈。</p>

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
                <!-- 加入了简书 -->
                <li id="feed-220309088">
                    <div class="content">
                        <div class="author author-restyle">
                            <a class="avatar" href="#">
                                <img src="../../../assets/img/头像.jpg"
                                    alt="180">
                            </a>
                            <div class="info">
                                <a class="nickname" href="#">超凡</a>
                                <span data-type="join_jianshu" data-datetime="2017-11-18T09:36:57+08:00"> 加入了简书 · 2017.11.18 09:36</span>
                            </div>
                        </div>
                    </div>
                </li>
            </ul>

        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {

            }
        },
        components: {
        }
    }
</script>
<style scoped>
    @media (min-width: 992px) {
        .container {
            width: 960px;
        }
    }

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

    .trigger-menu li:after,
    .trigger-menu li:hover:after {
        -webkit-transition: .2s ease-in-out;
    }

    .trigger-menu li:after {
        content: "";
        position: absolute;
        left: 50%;
        bottom: -2px;
        width: 100%;
        opacity: 0;
        border-bottom: 2px solid #646464;
    }

    .trigger-menu i {
        margin-right: 5px;
        font-size: 17px;
    }

    .trigger-menu li.active {
        border-bottom: 2px solid #646464;
    }

    .note-list {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .note-list li.have-img {
        min-height: 140px;
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

    .note-list .have-img .wrap-img img {
        width: 100%;
        height: 100%;
        border-radius: 4px;
        border: 1px solid #f0f0f0;
    }

    .note-list .have-img>div {
        padding-right: 160px;
    }

    .note-list .author {
        margin-bottom: 14px;
        font-size: 13px;
    }

    .note-list .author .avatar,
    .note-list .author .info {
        display: inline-block;
        vertical-align: middle;
        margin: 0 5px 0 0;
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

    .note-list .abstract {
        margin: 0 0 8px;
        font-size: 13px;
        line-height: 24px;
    }

    .note-list .meta {
        padding-right: 0!important;
        font-size: 12px;
        font-weight: 400;
        line-height: 20px;
    }

    .note-list .origin-author {
        display: inline;
        margin-bottom: 5px;
        font-size: 12px;
        color: #969696;
    }

    .note-list .meta a {
        margin-right: 10px;
        color: #b4b4b4;
    }

    .note-list .meta span {
        margin-right: 10px;
        color: #b4b4b4;
    }

    .note-list .author-restyle {
        margin-bottom: 0;
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