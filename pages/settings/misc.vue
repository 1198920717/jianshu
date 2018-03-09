<template>
    <div>
        <my-header></my-header>
        <div class="container notification setting">
            <div class="row">
                <div class="aside">
                    <ul>
                        <li>
                            <nuxt-link to="basic">
                                <i class="fa fa-list-ul"></i>
                                <span>基础设置</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="profile">
                                <i class="fa fa-vcard-o"></i>
                                <span>个人资料</span>
                            </nuxt-link>
                        </li>
                        <li style="background: #eee;">
                            <nuxt-link to="misc">
                                <i class="fa fa-pinterest-p"></i>
                                &nbsp;
                                <span>&nbsp;微博认证</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
                                <i class="fa fa-ban"></i>
                                &nbsp;
                                <span>黑名单</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="">
                                <i class="fa fa-yen"></i>
                                &nbsp;
                                <span>&nbsp;&nbsp;赞赏设置</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa fa-cog"></i>
                                &nbsp;
                                <span>账号管理</span>
                            </a>
                        </li>
                    </ul>
                </div>


                <div class="col-xs-16 col-xs-offset-8 main">
                    <img src="../../assets/img/微博认证.png" class="weibo-auth-img">
                    <div class="certification">
                        <div class="title">简书新浪微博联合认证</div>
                        <span>简书推荐作者</span>
                        <ul>
                            <li>
                                <i class="fa fa-check"></i>
                                简书帐号注册超过 30 天
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                简书帐号绑定新浪微博帐号
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                绑定手机号码
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                在简书发表文章字数达到 20000 字
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                在简书收获喜欢数达到 2000 个
                            </li>
                        </ul>
                        <!---->
                    </div>
                    <div class="certification">
                        <div class="title">简书新浪微博联合认证</div>
                        <span>简书专题运营者</span>
                        <ul>
                            <li>
                                <i class="fa fa-check"></i>
                                简书帐号注册超过 30 天
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                简书帐号绑定新浪微博帐号
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                绑定手机号码
                            </li>
                            <li>
                                <i class="fa fa-minus"></i>
                                在简书参与编辑的专题收获订阅总数达到 1000 个
                            </li>
                        </ul>
                        <!---->
                    </div>
                    <!---->
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



    .notification .aside ul span {
        font-size: 15px;
        vertical-align: middle;
    }




    .col-xs-offset-8 {
        margin-left: 33.33333%;
    }

    .col-xs-16 {
        width: 66.66667%;
        float: left;
        position: relative;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
    }

    .setting .main .weibo-auth-img {
        margin: 0 0 30px -12px;
        width: 450px;
        height: 216px;
    }

    img {
        vertical-align: middle;
    }

    img {
        border: 0;
    }

    .setting .main .certification {
        margin-bottom: 40px;
    }

    .setting .main .certification .title {
        font-size: 15px;
        font-weight: 700;
        display: inline-block;
        vertical-align: middle;
    }

    .setting .main .certification span {
        font-size: 15px;
        color: #969696;
    }

    .setting .main span {
        margin: 0 20px 0 6px;
        font-size: 15px;
        vertical-align: middle;
    }

    .setting .main .certification ul {
        margin: 15px 0;
        list-style: none;
    }

    .setting .main .certification li {
        font-size: 15px;
        line-height: 30px;
    }

    .setting .main .certification .fa-check {
        margin-right: 5px;
        color: #42c02e;
    }
</style>