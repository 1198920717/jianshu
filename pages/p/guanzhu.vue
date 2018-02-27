<template>
    <div>
        <my-header></my-header>
        <div class="container notification">
            <div class="row">
                <div class="aside">
                    <ul>
                        <li>
                            <nuxt-link to="/p/pinglun">
                                <i class="fa fa-comment-o"></i>
                                <span>评论</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/p/jianxin">
                                <i class="fa fa-envelope-o"></i>
                                <span>简信</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/p/tougaoqingqiu">
                                <i class="fa fa-upload"></i>
                                <span>投稿请求</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/p/xihuanhezan">
                                <i class="fa fa-heart-o"></i>
                                <span>喜欢和赞</span>
                            </nuxt-link>
                        </li>
                        <li style="background: #eee;">
                            <nuxt-link to="/p/guanzhu">
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
                        <div class="menu">全部关注</div>
                        <ul class="follow-list">
                            <li class="">
                                <a href="#" class="avatar">
                                    <img src="../../assets/img/头像.jpg">
                                </a>
                                <div class="info">
                                    <a href="#" class="user">优雅的姑娘</a>
                                    <span>关注了你</span>
                                    <div class="time">2018.01.30 15:33</div>
                                </div>
                                <a class="btn btn-success follow">
                                    <i class="fa fa-plus"></i>
                                    <span>关注</span>
                                </a>
                            </li>
                            <div class="notification-list-placeholder" style="display: none;">
                                <div class="avatar"></div>
                                <div class="wrap">
                                    <div class="btn"></div>
                                    <div class="name"></div>
                                    <div class="text"></div>
                                </div>
                                <p></p>
                                <p class="animation-delay"></p>
                                <div class="meta">
                                    <i class="iconfont ic-list-comments"></i>
                                    <div class="text"></div>
                                    <i class="iconfont ic-go"></i>
                                    <div class="text longer"></div>
                                </div>
                            </div>
                        </ul>
                        <div class="find-nothing">
                            <img src="../../assets/img/这里还没有内容哦.png" alt="">
                            <div>这里还没有内容哦~</div>
                        </div>
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
        display: none;
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

    .notification .main .follow-list li {
        padding: 20px;
        border-top: 1px solid #f0f0f0;
    }

    li {
        line-height: 20px;
    }

    .notification .main .follow-list .avatar {
        display: inline-block;
        margin-right: 5px;
        width: 40px;
        height: 40px;
        cursor: pointer;
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
    .notification .main .follow-list .info {
    max-width: 420px;
}
.notification .main .follow-list .info{
    display: inline-block;
    vertical-align: top;
    width: 535px;
    font-size: 0;
    line-height: 1.7;
}
.notification .main .follow-list .info .user{
    margin: 0 5px 0 0;
    color: #333;
}
.notification .main .follow-list .info a{
    font-size: 15px;
}
a {
    cursor: pointer;
}
.notification .main .follow-list .info span{
    font-size: 15px;
}
.notification .main .follow-list .time{
    margin-top: 2px;
    font-size: 12px;
    color: #969696;
    line-height: normal;
}
.notification .main .follow-list .btn {
    padding: 8px 0;
    width: 100px;
    float: right;
    font-size: 15px;
}

.follow {
    border-color: #42c02e;
}
.follow, .follow-cancel, .follow-each, .following {
    font-weight: 400;
    line-height: normal;
}
.btn-success {
    border-radius: 40px;
    color: #fff!important;
    background-color: #42c02e;
}
.iconfont {
    font-family: iconfont!important;
    font-size: inherit;
    font-style: normal;
    font-weight: 400!important;
}
.follow span {
    margin-left: 2px;
    display: inline;
}
</style>