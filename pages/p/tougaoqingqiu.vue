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
                        <li style="background: #eee;">
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
                        <li>
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
                        <div class="menu">全部投稿请求</div>
                        <ul class="push-list">
                            <li>
                                <a href="#" class="wrap">
                                    <div class="all-push">
                                        <i class="fa fa-upload"></i>
                                    </div>
                                    <div class="name">全部未处理请求</div>
                                </a>
                            </li>
                            <div class="jianxin-placeholder request" style="display: none;">
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

    .notification .main .push-list li {
        border-top: 1px solid #f0f0f0;
    }

    li {
        line-height: 20px;
    }
    .notification .main .push-list .wrap {
    padding: 20px;
    display: block;
}
.notification .main .push-list .all-push {
    position: relative;
    margin-right: 10px;
    width: 48px;
    height: 48px;
    text-align: center;
    border: 1px solid #f4f4f4;
    border-radius: 4px;
    display: inline-block;
    vertical-align: middle;
}
.notification .main .push-list .name {
    max-width: 500px;
    font-size: 15px;
    vertical-align: middle;
    display: inline-block;
}
.notification .main .push-list .all-push i {
    margin-top: 14px;
    font-size: 25px;
    color: #ea6f5a;
    display: block;
}

.iconfont {
    font-family: iconfont!important;
    font-style: normal;
    font-weight: 400!important;
}
</style>