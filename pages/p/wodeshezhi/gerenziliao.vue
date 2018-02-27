<template>
    <div>
        <my-header></my-header>
        <div class="container notification setting">
            <div class="row">
                <div class="aside">
                    <ul>
                        <li style="background: #eee;">
                            <nuxt-link to="/p/wodeshezhi/jichushezhi">
                                <i class="fa fa-list-ul"></i>
                                <span>基础设置</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/p/wodeshezhi/gerenziliao">
                                <i class="fa fa-vcard-o"></i>
                                <span>个人资料</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/p/wodeshezhi/weiborenzheng">
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
                    <table>
                        <thead>
                            <tr>
                                <th class="setting-head"></th>
                                <th></th>
                            </tr>
                        </thead>
                        <tbody class="information">
                            <tr>
                                <td class="top-line setting-title setting-verticle">
                                    性别
                                </td>
                                <td class="top-line">
                                    <input type="radio" value="1">
                                    <span>男</span>
                                    <input type="radio" value="2">
                                    <span>女</span>
                                    <input type="radio" value="0">
                                    <span>保密</span>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title pull-left">个人简介</td>
                                <td>
                                    <form>
                                        <textarea placeholder="填写你的个人简介"></textarea>
                                    </form>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title pull-left setting-input">个人网站</td>
                                <td>
                                    <form>
                                        <input type="text" name="website" placeholder="http://你的网址">
                                        <p class="pull-right">填写后会在个人主页显示图标</p>
                                    </form>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title">微信二维码</td>
                                <td class="weixin-qrcode">
                                    <input type="file" class="hide">
                                    <a class="btn btn-hollow">
                                        <input type="file" class="hide"> 更换图片
                                    </a>
                                    <p class="pull-right">上传后会在个人主页显示图标</p>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title setting-input pull-left">社交帐号</td>
                                <td class="social-bind">
                                    <p>你可以通过绑定的社交帐号登录简书。出于安全因素, 你最初用来创建账户的社交帐号不能移除。</p>
                                    <p>如果帐号被占用，你可以在
                                        <a href="#">简书帐号绑定解绑相关问题汇总</a>中获得相关帮助。</p>
                                    <ul class="social-bind-list">
                                        <li>
                                            <div class="bind-name">
                                                <i class="fa fa-weibo"></i>
                                                <a href="#">绑定微博
                                                    <i class="fa fa-angle-right"></i>
                                                </a>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="bind-name">
                                                <i class="fa fa-wechat"></i>
                                                <a href="#">绑定微信
                                                    <i class="fa fa-angle-right"></i>
                                                </a>
                                            </div>
                                        </li>
                                        <li class="has-bind">
                                            <div class="bind-name">
                                                <i class="fa fa-qq"></i>
                                                <a href="#">绑定qq
                                                    <i class="fa fa-angle-right"></i>
                                                </a>
                                            </div>
                                            <!---->
                                        </li>
                                        <li>
                                            <div class="bind-name">
                                                <i class="fa fa-renren"></i>
                                                <a href="#">绑定豆瓣
                                                    <i class="fa fa-angle-right"></i>
                                                </a>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="bind-name">
                                                <i class="fa fa-google-plus"></i>
                                                <a href="#">绑定 Google+
                                                    <i class="fa fa-angle-right"></i>
                                                </a>
                                            </div>
                                        </li>
                                    </ul>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                    <input type="submit" class="btn btn-success setting-save" value="保存">
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
        width: 700px;
        height: 295px;
        margin-left: 37.33%;
        position: relative;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
    }
    table {
        border-collapse: collapse;
    }
    .setting .main tr {
        border-bottom: 1px solid #f0f0f0;
    }
    .setting .main tr:last-child {
        border: none;
    }
    .setting .main .setting-verticle {
        vertical-align: bottom;
    }
    .setting .main .setting-title {
        width: 150px;
        font-size: 15px;
        color: #969696;
    }
    .setting .main .top-line {
        padding-top: 0;
    }
    .setting .main td {
        padding: 20px 0;
    }
    button,
    input,
    select,
    textarea {
        font-family: inherit;
        font-size: inherit;
        line-height: inherit;
    }
    input {
        line-height: normal;
    }
    button,
    input,
    optgroup,
    select,
    textarea {
        color: inherit;
        font: inherit;
        margin: 0;
    }
    .setting .main span {
        margin: 0 20px 0 6px;
        font-size: 15px;
        vertical-align: middle;
    }
    .setting .main textarea {
        width: 100%;
        height: 100px;
        margin-bottom: 10px;
        padding: 8px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0, 0%, 71%, .1);
        display: block;
        resize: none;
        outline-style: none;
    }
    .setting .main .information input[name=website] {
        width: 100%;
        margin-bottom: 10px;
    }
    .setting .main input[type=email],
    .setting .main input[type=text] {
        padding: 5px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0, 0%, 71%, .1);
    }
    .setting .main p {
        margin: 0;
        padding: 8px 0 0;
        font-size: 12px;
        color: #969696;
        clear: both;
    }
    .pull-right {
        float: right!important;
    }
    .setting .main .hide {
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }
    .setting .main .btn-delete,
    .setting .main .btn-hollow {
        font-size: 14px;
    }
    .btn-hollow {
        border: 1px solid rgba(59, 194, 29, .7);
        color: #42c02e!important;
    }
    .btn-delete,
    .btn-gray,
    .btn-hollow {
        padding: 4px 12px;
        font-size: 12px;
        font-weight: 400;
        line-height: normal;
        border-radius: 40px;
        background: none;
    }
    .setting .main p a {
        color: #3194d0!important;
    }
    .setting .main .information .social-bind-list {
        margin: 0;
        list-style: none;
    }
    .setting .main .information .social-bind-list li {
        border-bottom: 1px solid #f0f0f0;
        line-height: 50px;
    }
    .setting .main .information .social-bind-list li:last-child {
        border: none;
    }
    .setting .main .information .social-bind-list .bind-name {
        display: inline-block;
    }
    .setting .main .information .social-bind-list i {
        width: 30px;
        font-size: 20px;
        vertical-align: middle;
        display: inline-block;
    }
    .setting .main .information .fa-weibo {
        color: #ea6f5a;
    }
    .setting .main .information .fa-wechat {
        color: #42c02e;
    }
    .setting .main .information .fa-qq {
        color: #3194d0;
    }
    .setting .main .information .fa-renren {
        color: #42c02e;
    }
    .setting .main .information .fa-google-plus {
        color: #ec6149;
    }
    .setting .main .information .social-bind-list .bind-name a {
        margin: 0 0 0 20px;
        font-size: 14px;
        vertical-align: middle;
    }
    .setting .main .information .social-bind-list .bind-name .fa-angle-right {
        font-size: 14px;
    }
    .main .setting-save {
        width: 100px;
        margin: 30px 0 60px;
        border-radius: 20px;
        border: none;
    }
    .btn-success {
        border-radius: 40px;
        color: #fff;
        background-color: #42c02e;
        border-color: #42c02e;
    }
    .btn {
        display: inline-block;
        font-weight: 400;
        text-align: center;
        vertical-align: middle;
        touch-action: manipulation;
        background-image: none;
        white-space: nowrap;
        padding: 6px 12px;
        font-size: 14px;
        line-height: 1.42857;
        user-select: none;
    }
</style>