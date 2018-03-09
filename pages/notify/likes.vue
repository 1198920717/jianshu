<template>
    <div>
        <my-header></my-header>
        <div class="container notification">
            <div class="row">
                <div class="aside">
                    <ul>
                        <li>
                            <nuxt-link to="comments">
                                <i class="fa fa-comment-o"></i>
                                <span>评论</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="chats">
                                <i class="fa fa-envelope-o"></i>
                                <span>简信</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="requests">
                                <i class="fa fa-upload"></i>
                                <span>投稿请求</span>
                            </nuxt-link>
                        </li>
                        <li style="background: #eee;">
                            <nuxt-link to="likes">
                                <i class="fa fa-heart-o"></i>
                                <span>喜欢和赞</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="follows">
                                <i class="fa fa-user-o"></i>
                                <span>&nbsp;关注</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
                                &nbsp;
                                <i class="fa fa-rmb"></i>
                                <span>赞赏和付费</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
                                <i class="">· · ·</i>
                                <span>其他提醒</span>
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <div class="main">
                    <div>
                        <div class="menu">收到的喜欢和赞</div>
                        <ul class="comment-list">
                            <li class="aaa">
                                <a href="/u/5b3e3040b3ab" class="avatar">
                                    <img src="../../assets/img/头像.jpg">
                                </a>
                                <div class="info">
                                    <div>
                                        <a class="user" href="/u/5b3e3040b3ab">爱的华尔兹_4968</a>
                                        <span class="comment-slogan">评论了你的文章</span>
                                        <a href="/p/ea2478dc4e62">《万世天下第一》</a>
                                    </div>
                                    <div class="time">2018.03.01 18:03</div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../../components/myHeader'
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
    @media (max-width: 1080px) {
        .container {
            width: 750px;
        }
    }

    @media (min-width: 768px) {
        .container {
            width: 750px;
        }
    }

    div {
        display: block;
    }

    .container {
        margin-right: auto;
        margin-left: auto;
        padding-left: 15px;
        padding-right: 15px;
    }

    .notification .row {
        padding: 30px 0;
        margin-left: -125px;
    }

    .row {
        margin-left: -15px;
        margin-right: -15px;
    }

    .notification .aside {
        position: fixed;
        top: 0;
        bottom: 0;
        margin: 86px 0 0;
        padding: 0 0 30px;
        width: 280px;
        overflow: auto;
    }

    .notification .aside ul {
        list-style: none;
    }

    .notification .aside ul li {
        margin: 0;
    }

    .notification .aside ul li:hover {
        background: #eee;
    }

    li {
        line-height: 51px;
    }

    .notification .aside ul li.active a {
        background-color: #f0f0f0;
        border-radius: 4px;
    }

    .notification .aside ul a {
        height: auto;
        padding: 10px 25px;
        line-height: 30px;
        display: block;
    }

    a {
        cursor: pointer;
        color: #333;
        text-decoration: none;
    }

    .notification .aside ul i {
        margin-right: 15px;
        font-size: 24px;
        color: #ea6f5a;
        vertical-align: middle;
    }

    .iconfont {
        font-family: iconfont!important;
        font-style: normal;
        font-weight: 400!important;
    }

    .notification .aside ul span {
        font-size: 15px;
        vertical-align: middle;
    }

    .main {
        padding-left: 0;
        width: 640px;
        height: 295px;
        margin-left: 37.33%;
        position: relative;
    }

    .main .menu {
        margin-bottom: 20px;
        font-size: 14px;
        font-weight: 700;
    }

    .a {
        background-color: #ccc;
    }

    .main .find-nothing {
        margin-top: 150px;
        text-align: center;
    }

    .main .find-nothing img {
        width: 100px;
        vertical-align: middle;
        border: 0;
    }

    .main .find-nothing div {
        margin-top: 20px;
        font-size: 14px;
        font-weight: 700;
    }



       .notification .main ul {
        list-style: none;
    }

    .notification .main .comment-list li {
        padding: 20px;
        border-top: 1px solid #f0f0f0;
    }

    li {
        line-height: 20px;
    }

    .notification .main .comment-list .avatar {
        display: inline-block;
        margin-right: 5px;
        width: 40px;
        height: 40px;
    }

    .notification .main .comment-list .info {
        display: inline-block;
        vertical-align: top;
        width: 535px;
        font-size: 0;
        line-height: 1.7;
    }

    .notification .main .comment-list .time {
        margin-top: 2px;
        font-size: 12px;
        color: #969696;
        line-height: normal;
    }

    .notification .main .comment-list .info .user {
        margin: 0 5px 0 0;
        color: #333!important;
        font-size: 15px;
    }

    .notification .main .comment-list .info .comment-slogan {
        font-size: 15px;
        color: #333;
    }

    .notification .main .comment-list .info a {
        font-size: 15px;
        color: #3194d0!important;
    }
</style>
