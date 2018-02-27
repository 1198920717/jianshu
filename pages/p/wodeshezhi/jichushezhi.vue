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
                                <th class="setting-head responsive-head"></th>
                                <th></th>
                            </tr>
                        </thead>
                        <tbody class="base">
                            <tr>
                                <td class="top-line">
                                    <div class="avatar">
                                        <img src="../../../assets/img/头像.jpg">
                                    </div>
                                </td>
                                <td class="top-line">
                                    <a class="btn btn-hollow">
                                        <input unselectable="on" type="file" class="hide"> 更改头像
                                    </a>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title">
                                    昵称
                                </td>
                                <td>
                                    <input type="text" placeholder="请输入昵称">
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title">电子邮件</td>
                                <td>
                                    <form>
                                        <input type="button" value="发送" class="btn btn-hollow pull-right">
                                        <input type="email" placeholder="请输入你的常用邮箱">
                                    </form>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title">手机</td>
                                <td>
                                    <input type="submit" class="btn btn-hollow" value="绑定手机">
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title setting-editor">常用编辑器</td>
                                <td>
                                    <div class="col-xs-8">
                                        <input type="radio" value="plain" checked>
                                        <span>富文本</span>
                                    </div>
                                    <div class="col-xs-16">
                                        <input type="radio" value="markdown">
                                        <span>Markdown
                                            <a href="#" target="_blank" class="help">
                                                <i class="iconfont ic-navigation-help"></i>
                                            </a>
                                        </span>
                                    </div>
                                    <p>切换后对新建文章生效</p>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title setting-verticle">语言设置</td>
                                <td>
                                    <div class="col-xs-8">
                                        <input type="radio" value="zh-CN" checked>
                                        <span>中文简体</span>
                                    </div>
                                    <div class="col-xs-16">
                                        <input type="radio" value="zh-TW">
                                        <span>中文繁体</span>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title setting-verticle">接收谁的简信</td>
                                <td>
                                    <div class="col-xs-8">
                                        <input type="radio" value="true" checked>
                                        <span class="responsive-span">所有人</span>
                                    </div>
                                    <div class="col-xs-16">
                                        <input type="radio" value="false">
                                        <span class="responsive-span">我关注的人、我发过简信的人</span>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="setting-title setting-verticle">提醒邮件通知</td>
                                <td>
                                    <div class="col-xs-8">
                                        <input type="radio" value="instantly" checked>
                                        <span class="responsive-span">所有动态</span>
                                    </div>
                                    <div class="col-xs-11">
                                        <input type="radio" value="later">
                                        <span class="responsive-span">每天未读汇总</span>
                                    </div>
                                    <div class="col-xs-5">
                                        <input type="radio" value="none">
                                        <span class="responsive-span">不接收</span>
                                    </div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                    <input type="submit" class="btn btn-success setting-save" value="保存">
                    <!---->
                    <!---->
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
        padding-left: 0;
        width: 700px;
        height: 295px;
        margin-left: 37.33%;
        position: relative;
    }




    .setting .main table {
        width: 100%;
    }

    table {
        background-color: transparent;
    }

    table {
        border-collapse: collapse;
        border-spacing: 0;
    }

    tbody {
        display: table-row-group;
        vertical-align: middle;
        border-color: inherit;
    }

    .setting .main .base tr:first-child {
        border: none;
    }

    .setting .main tr {
        border-bottom: 1px solid #f0f0f0;
    }

    .setting .main tr:last-child {
        border: none;
    }

    .setting .main .setting-title {
        font-size: 15px;
        color: #969696;
    }

    .setting .main .top-line {
        padding-top: 0;
    }

    .setting .main td {
        padding: 20px 0;
    }

    .setting .main .avatar {
        width: 100px;
        height: 100px;
    }

    .avatar {
        width: 32px;
        height: 32px;
        display: block;
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

    .setting .main .hide {
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }

    .setting .main input[type=email] {
        width: 280px;
    }

    .col-xs-8 {
        width: 33.33333%;
        padding: 0;
        float: left;
    }

    .col-xs-11 {
        width: 33.33333%;
        padding: 0;
        float: left;
    }

    .setting .main p {
        margin: 0;
        padding: 8px 0 0;
        font-size: 12px;
        color: #969696;
        clear: both;
    }

    input[type=checkbox],
    input[type=radio] {
        margin: 4px 0 0;
        margin-top: 1px\9;
        line-height: normal;
    }

    input[type=checkbox],
    input[type=radio] {
        box-sizing: border-box;
        padding: 0;
    }

    .setting .main span {
        margin: 0 20px 0 6px;
        font-size: 15px;
        vertical-align: middle;
    }



    .setting .main td {
        padding: 20px 0;
    }

    .setting .main td {
        padding: 20px 0;
    }

    .setting .main input[type=email],
    .setting .main input[type=text] {
        padding: 5px 10px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0, 0%, 71%, .1);
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