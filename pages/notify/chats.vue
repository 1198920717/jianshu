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
                        <li style="background: #eee;">
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
                        <li>
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
                        <div class="menu">全部简信</div>
                        <ul class="jianxin-list">
                            <li>
                                <div class="pull-right">
                                    <span class="time">2017.11.19 09:37</span>
                                    <div>
                                        <a href="javascript:void(0);" @click="showToggle">
                                            <i class="fa fa-angle-down"></i>
                                        </a>
                                        <ul v-show="isShow" class="xianshi">
                                            <li>
                                                <a>
                                                    <i class="fa fa-trash-o"></i>删除会话</a>
                                            </li>
                                            <li>
                                                <a>
                                                    <i class="fa fa-ban"></i>加入黑名单</a>
                                            </li>
                                            <li>
                                                <a>
                                                    <i class="fa fa-flag-o"></i>举报用户
                                                </a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                                <a href="#" target="_blank" class="avatar">
                                    <img src="../../assets/img/头像.jpg">
                                    <!---->
                                </a>
                                <a href="#" target="_blank" class="name">简宝玉</a>
                                <a href="#" class="wrap">
                                    <p> 欢迎加入丰富多彩的原创内容社区——简书。有任何疑问（如何投稿，专题主编，签约作者，简叔，简小...</p>
                                </a>
                            </li>
                            <div class="jianxin-placeholder" style="display: none;">
                                <div class="avatar"></div>
                                <div class="wrap">
                                    <div class="time"></div>
                                    <div class="name"></div>
                                    <div class="text"></div>
                                </div>
                            </div>
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
                isShow: false
            }
        },
        methods: {
            showToggle: function () {
                this.isShow = !this.isShow
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

    .main ul {
        list-style: none;
    }

    .main .jianxin-list li {
        position: relative;
        border-top: 1px solid #f0f0f0;
        line-height: 20px;
    }

    .pull-right {
        float: right!important;
    }

    .main .jianxin-list .avatar {
        float: left;
        margin: 20px 10px 20px 20px;
        width: 48px;
        height: 48px;
    }

    .avatar {
        display: block;
        cursor: pointer;
    }

    .notification .main .jianxin-list .name {
        position: absolute;
        top: 25px;
        font-size: 15px;
    }

    .notification .main .jianxin-list .wrap {
        display: block;
        padding: 20px 20px 20px 0;
        min-height: 88px;
    }

    .share-group .hahaha1,
    .hahaha2,
    .hahaha3,
    span {
        line-height: 30px;
        font-size: 14px;
    }

    .notification .main .jianxin-list .pull-right .time {
        color: #9b9b9b;
    }

    .notification .main .jianxin-list .pull-right {
        margin: 20px 20px 0 0;
        font-size: 13px;
    }

    .notification .main .jianxin-list .pull-right div {
        display: inline;
    }

    .notification .main .dropdown-menu {
        top: auto;
        left: auto;
        right: 15px;
        color: #333;
        min-width: inherit;
    }


    .notification .main .jianxin-list p {
        margin: 28px 0 0;
        font-size: 12px;
        color: #999;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    .notification .main .xianshi {
        right: 15px;
        position: absolute;
        padding: 5px 0;
        font-size: 14px;
        background-color: #fff;
        border: 1px solid rgba(0, 0, 0, .15);
        border-radius: 4px;
    }

    .notification .main .xianshi li {
        border: none!important;
        position: relative;
    }

    .notification .main .jianxin-list .xianshi a {
        padding: 10px 20px;
    }

    .xianshi>li>a {
        display: block;
        padding: 3px 20px;
        clear: both;
        font-weight: 400;
        line-height: 1.42857;
        color: #333;
        white-space: nowrap;
    }

    .notification .main .xianshi i {
        margin-right: 10px;
    }
</style>