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
                            <li class="active">
                                <nuxt-link to="guanzhudezhuanti">
                                    关注的专题/文集/连载 0
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="xihuandewenzhang">
                                    喜欢的文章 1
                                </nuxt-link>
                            </li>
                        </ul>

                        <div id="list-container">
                            <ul class="user-list">
                                <li class="paid-notebook-item">
                                    <a class="avatar-collection" href="#">
                                        <img src="../../../assets/img/文集.png" alt="Avatar notebook default">
                                    </a>
                                    <div class="info">
                                        <a class="name" href="#">文集</a>
                                        <div class="meta">
                                            收录了40篇文章，1人关注
                                        </div>
                                    </div>
                                    <a class="btn btn-default following">
                                        <i class="fa fa-check"></i>
                                        <span>已关注</span>
                                    </a>
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

    .person .main .user-list {
        list-style: none;
        clear: both;
    }

    .person .main .user-list li:first-child {
        padding-top: 0!important;
    }

    .person .main .user-list li {
        padding-bottom: 20px;
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        line-height: normal;
    }

    .person .main .user-list .paid-notebook-item .avatar-collection {
        height: 70px;
    }

    .person .main .user-list .avatar,
    .person .main .user-list .avatar-collection {
        width: 52px;
        height: 52px;
        margin-right: 8px;
        vertical-align: middle;
        display: inline-block;
    }

    .avatar-collection img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 10%;
    }

    .person .main .user-list .info {
        vertical-align: middle;
        display: inline-block;
        max-width: 450px;
    }

    .person .main .user-list .info a,
    .person .main .user-list .name {
        font-size: 15px;
        font-weight: 700;
        color: #333;
    }

    .person .main .user-list .meta {
        padding-top: 2px;
        font-size: 12px;
        color: #969696;
    }

    .person .main .user-list .following {
        float: right;
        margin-top: 8px;
        padding: 8px 0;
        width: 100px;
        font-size: 15px;
    }

    .following {
        border: 1px solid hsla(0, 0%, 59%, .6);
        background: none;
    }

    .btn-default {
        border-radius: 40px;
        color: #8c8c8c;
    }

    .following span {
        margin-left: 2px;
        display: inline;
        color: #8c8c8c;
    }

    .following .fa-check {
        color: #8c8c8c;
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