<template>
    <div>
        <div id="comment-list" class="comment-list">
            <!-- 提交的表单 -->
            <form class="new-comment">
                <nuxt-link class="avatar" to="/u/213">
                    <img src="../assets/img/default.avatar.jpg">
                </nuxt-link>
                <textarea @focus="sendCommentBtn=true" placeholder="写下你的评论" v-model="commentData"></textarea>
                <transition :duration="200" name="fade">
                    <div v-if="sendCommentBtn" class="write-function-block clearfix">
                        <div class="emoji-modal-wrap">
                            <a href="javascript:void(0)" @click="showEmoji=!showEmoji" class="emoji">
                                <i class="fa fa-smile-o"></i>
                            </a>
                            <transition :duration="200" name="fade">
                                <div v-if="showEmoji" class="emoji-modal arrow-up">
                                    <vue-emoji @select="selectEmoji"></vue-emoji>
                                </div>
                            </transition>
                        </div>
                        <div class="hint">
                            Ctrl+Enter 发表
                        </div>
                        <a class="btn btn-send" href="javascript:void(0)" @click="sendComment">发送</a>
                        <a class="cancel" href="javascript:void(0)" @click="sendCommentBtn=false">取消</a>
                    </div>
                </transition>
            </form>
            <!-- 留言的列表 -->
            <div id="normal-comment-list" class="normal-comment-list">
                <!-- 留言的排序 -->
                <div class="top-title">
                    <span>25条评论</span>
                    <a class="author-only" href="javascript:void(0);">只看作者</a>
                    <div class="pull-right">
                        <a class="active" href="javascript:void(0);" v-on:click="sort1">按喜欢排序</a>
                        <a class="active" href="javascript:void(0);" v-on:click="sort">按时间正序</a>
                        <a class="active" href="javascript:void(0);" v-on:click="reverse">按时间倒序</a>
                    </div>
                </div>
                <!-- 留言的正文 -->
                <div class="comment-placeholder" style="display:none;">
                    <div class="author">
                        <div class="avatar"></div>
                        <div class="info">
                            <div class="name"></div>
                            <div class="meta"></div>
                        </div>
                    </div>
                    <div class="title"></div>
                    <div class="title animated-delay"></div>
                    <div class="tool-group">
                        <i class="fa fa-thunbs-up"></i>
                        <div class="zan"></div>
                        <i class="fa fa-comment"></i>
                        <div class="like"></div>
                    </div>
                </div>
                <div :id="'comment-'+comment.id" v-for="(comment,index) in comments" class="comment">
                    <div class="comment-content">
                        <div class="author">
                            <nuxt-link class="avatar" to="/u/123" @mouseover.native="commentBtn(comment.id)">
                                <div class="geren-kuang" v-show="as">
                                    <div class="kuang-shang">
                                        <img :src="comment.user.avatar">
                                        <div class="kuang-shang-1">
                                            <p class="a">夜语可书</p>
                                            <p class="b">断桥守望者</p>
                                            <p class="c">三世断桥之青丘镜殇 第九章 马头族</p>
                                            <p class="c">仿树下野狐《刹那芳华曲》</p>
                                            <p class="c">三世断桥之青丘镜殇 第八章 追风系</p>
                                        </div>
                                    </div>
                                    <div class="kuang-xia">
                                        <div class="kuang-xia-1">
                                            <div class="kuang-xia-1-1">
                                                <p class="aa">32</p>
                                                <p>文章</p>
                                            </div>
                                            <div class="kuang-xia-1-1">
                                                <p class="aa">70</p>
                                                <p>关注</p>
                                            </div>
                                            <div class="kuang-xia-1-1">
                                                <p class="aa">270</p>
                                                <p>粉丝</p>
                                            </div>
                                        </div>
                                        <div class="kuang-xia-2">
                                            <nuxt-link to="/u/123" class="jianxin">发简信</nuxt-link>
                                            <a href="javascript:void(0);" class="btn btn-success">
                                                <i class="fa"></i>
                                                <span ref="followWord2">关注</span>
                                            </a>
                                        </div>
                                    </div>
                                    <div class="sanjiao"></div>
                                </div>
                                <img :src="comment.user.avatar" @mouseover="as=true" @mouseleave="as=false">
                            </nuxt-link>
                            <div class="info">
                                <nuxt-link to="/u/123" class="name">
                                    {{comment.user.nick_name}}
                                </nuxt-link>
                                <div class="meta">
                                    <span>
                                        {{comment.floor}}楼·{{comment.create_at | formDate}}
                                    </span>
                                </div>
                            </div>
                        </div>
                        <div class="comment-wrap">
                            <p>
                                {{comment.compiled_content}}
                            </p>
                            <div class="tool-group">
                                <a href="javascript:void(0);" :class="zanObj" @click="zan">
                                    <i class="fa fa-thumbs-o-up"></i>
                                    <a ref="span">34</a>
                                </a>
                                <a href="javascript:void(0);" @click="showSubCommentForm(index)">
                                    <i class="fa fa-comment-o"></i>
                                    <span>回复</span>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="sub-comment-list">
                        <div v-show="comment.children.length !== 0" v-for="(subComment,nindex) in comment.children"
                         :id="'comment-' + subComment.id" class="sub-comment" :keys="nindex">
                                <p>
                                    <nuxt-link to="/u/123">
                                        {{subComment.user.nick_name}}
                                    </nuxt-link>
                                    :
                                    <span v-html="subComment.compiled_content"></span>
                                </p>
                                <div class="sub-tool-group">
                                    <span>{{subComment.create_at|formDate}}</span>
                                    <a href="javascript:void(0);" @click="showSubCommentFormAtName(index,subComment.user.nick_name)">
                                        <i class="fa fa-comment-o"></i>
                                        <span>回复</span>
                                    </a>
                                </div>
                            <div class="sub-comment more-comment">
                                <a href="javascript:void(0);" class="add-comment-btn" @click="showSubCommentForm(index)">
                                    <i class="fa fa-pencil"></i>
                                    <span>添加新评论</span>
                                </a>
                            </div>
                        </div>
                        <!-- 要显示的表单 -->
                        <transition :duration="200" name="fade">
                            <form class="new-comment-1" v-if="activeIndex.includes(index)">
                                <textarea v-focus placeholder="写下你的评论" ref="content" v-model="subCommentList[index]"></textarea>
                                <div class="write-function-block clearfix">
                                    <div class="emoji-modal-wrap">
                                        <a href="javascript:void(0);" class="emoji" @click="showSubEmoji(index)">
                                            <i class="fa fa-smile-o"></i>
                                        </a>
                                        <transition :duration="200" name="fade">
                                            <div v-if="emojiIndex.includes(index)" class="emoji-modal arrow-up">
                                                <vue-emoji ref="emoji" @select="selectSubEmoji"></vue-emoji>
                                            </div>
                                        </transition>
                                    </div>
                                    <div class="hint">Ctrl+Enter 发表</div>
                                    <a href="javascript:void(0);" class="btn btn-send" @click="sendSubCommentData(index)">发送</a>
                                    <a href="javascript:void(0);" class="cancel" @click="closeSubComment(index)">取消</a>
                                </div>
                            </form>
                        </transition>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import vueEmoji from '~/components/vueEmoji'
    export default {
        name: 'myComment',
        data() {
            return {
                zanObj: {
                    'like': true,
                    'likeing': false
                },
                sendCommentBtn: false,
                showEmoji: false,
                commentData: '',
                as: false,
                send: false,
                comments: [
                    {
                        children: [
                            {
                                compiled_content: "葡萄成熟透",
                                created_at: "2018-01-31T11:20:01.000+08:00",
                                id: 20151117,
                                parent_id: 20151024,
                                user: {
                                    id: 6121595,
                                    slug: "3252cb3c0eba",
                                    nick_name: "可可西里里"
                                },
                                user_id: 6121595
                            }
                        ],
                        children_count: 1,
                        compiled_content: "好了，2017年所有的绘画总结就全部分享完了",
                        create_at: "2018-02-02T13:39:08.000+08:00",
                        floor: 2,
                        id: 1,
                        liked: true,
                        likes_count: 20,
                        note_id: 20354702,
                        user: {
                            avatar: '/default.avatar.jpg',
                            id: 6780849,
                            is_author: false,
                            nick_name: '七岁就很拽',
                            slug: "41eba95aca00",
                            badge: null,
                        },
                        user_id: 6780849,
                    },
                    {
                        children: [
                            {
                                compiled_content: "葡萄fbsdjbfjsd成熟透",
                                created_at: "2018-01-31T11:20:01.000+09:00",
                                id: 20152217,
                                parent_id: 20151014,
                                user: {
                                    id: 6121225,
                                    slug: "3252dc3c0eba",
                                    nick_name: "可可asjkdfjkasdfkds西里里"
                                },
                                user_id: 6111595
                            }
                        ],
                        children_count: 1,
                        compiled_content: "好了sdgdffdgffdfah",
                        create_at: "2018-02-02T13:40:08.000+09:00",
                        floor: 3,
                        id: 2,
                        liked: true,
                        likes_count: 22,
                        note_id: 20354732,
                        user: {
                            avatar: '/default.avatar.jpg',
                            id: 6780869,
                            is_author: false,
                            nick_name: '七岁就很拽',
                            slug: "41eba95acc00",
                            badge: null,
                        },
                        user_id: 6780859,
                    }
                ],
                activeIndex: [],
                emojiIndex: [],
                subCommentList: [],
                oldIndex:null
            }
        },
        methods: {
            selectEmoji: function (code) {
                this.showEmoji = false;
                this.commentData += code;
            },
            sendComment: function () {
                console.log('发送');
            },
            zan: function () {
                let word = this.$refs.span.innerHTML;
                this.zanObj.like = !this.zanObj.like;
                this.zanObj.likeing = !this.zanObj.likeing;
                this.$refs.span.innerHTML = word == '20' ? '30' : '20';
            },
            //翻转
            reverse() {
                this.comments.reverse();
            },
            //时间正序
            sort() {
                this.comments.sort((a, b) => {
                    return b.create_at < a.create_at;
                });
            },
            //喜欢排序的方法：
            sort1() {
                this.comments.sort((a, b) => {
                    return a.likes_count < b.likes_count;
                });
            },
            showSubCommentForm: function (value) {
                if (this.activeIndex.includes(value)) {
                    this.activeIndex.splice(this.activeIndex.indexOf(value),1);
                } else {
                    //清除掉表单内的内容
                    this.subCommentList[value] = '';
                    //将表情关掉
                    this.emojiIndex = [];
                    this.activeIndex.push(value);
                }
            },
            showSubCommentFormAtName:function(nvalue,value,name){
                if(this.oldIndex == nvalue){
                    //第二次点击
                    let index = 
                    this.activeIndex.splice(this.activeIndex.indexOf(value),1);
                    this.subCommentList[value] = '';
                }else{
                    //第一次点击
                    this.subCommentList[value] = '';
                    this.activeIndex.push(value);
                    this.emojiIndex = [];
                    this.subCommentList[value] += `@${name} `;
                    this.oldIndex = nvalue;
                }  
            },
            closeSubComment: function (value) {
                let index = this.activeIndex.indexOf(value);
                this.activeIndex.splice(index, 1);
                //清除掉表单内的内容
                this.subCommentList[value] = '';
            },
            sendSubCommentData: function (value) {
                let index = this.activeIndex.indexOf(value);
                this.activeIndex.splice(index, 1);
                //value是下标
                console.log(this.subCommentList[value]);
            },
            showSubEmoji(value) {
                if (this.emojiIndex.includes(value)) {
                    this.emojiIndex = [];
                } else {
                    this.emojiIndex = [];
                    this.emojiIndex.push(value);
                }
            },
            selectSubEmoji: function (code) {
                //当前下标
                let index = this.emojiIndex[0]
                //将表情所代表的code值放入表单当中
                if (this.subCommentList[index] == null) {
                    this.subCommentList[index] = '';
                }
                this.subCommentList[index] += code;
                //关掉emoji
                this.emojiIndex = []
                //聚焦一下
                document.get('')
            }
        },
        components: {
            vueEmoji,
        },
        filters: {
            formDate(value) {
                let now = new Date(value);
                let year = now.getFullYear();
                let month = (now.getMonth() + 1).toString().padStart(2, 0);
                let date = now.getDate().toString().padStart(2, 0);
                let hour = now.getHours().toString().padStart(2, 0);
                let minute = now.getMinutes().toString().padStart(2, 0);
                return `${year}.${month}.${date} ${hour}:${minute}`;
            }
        },
        directives: {
            "focus": {
                bind: function (el, binding, vnode, oldVnode) {
                    el.focus();
                },
                update: function (el, binding, vnode, oldVnode) {
                    el.focus();
                },
                inserted: function (el) {
                    el.focus();
                }
            }
        },
        watch: {
            subCommentList: function (val) {
                console.log(val);
            }
        }
    }
</script>
<style>
    .fade-enter-active,
    .fade-leave-active {
        opacity: 1;
        transition: .3s;
        -webkit-transition: .3s
    }

    .fade-enter,
    .fade-leave-to {
        opacity: 0;
        transform: translate3d(0, -5%, 0);
        -webkit-transform: translate3d(0, -5%, 0);
        transition: .3s;
        -webkit-transition: .3s
    }

    .note .post .comment-list {
        padding-top: 20px;
        margin-bottom: 200px;
        /*此效果一会删除*/
    }

    .note .post .comment-list .new-comment {
        position: relative;
        margin-left: 48px;
        margin-bottom: 20px;
        padding: 5px 0;
    }

    .note .post .comment-list .avatar {
        width: 38px;
        height: 38px;
        display: inline-block;
        margin-right: 5px;
    }

    .note .post .comment-list .geren-kuang {
        position: absolute;
        width: 460px;
        height: 264px;
        margin-top: -279px;
        margin-left: -200px;
        border-radius: 10px;
        background-color: white;
        border: 1px solid #ccc;
        box-shadow: 1px 1px 5px 5px #ccc;
    }

    .note .post .comment-list .geren-kuang .kuang-shang {
        width: 100%;
        height: 195px;
        border-bottom: 1px solid #eee;
    }

    .note .post .comment-list .geren-kuang .kuang-shang img {
        width: 80px;
        height: 80px;
        margin: 15px;
    }

    .note .post .comment-list .geren-kuang .kuang-shang .kuang-shang-1 {
        width: 320px;
        float: right;
        display: block;
        margin-top: 15px;
    }

    .note .post .comment-list .geren-kuang .kuang-shang .kuang-shang-1 p {
        margin: 0;
        padding: 0;
    }

    .note .post .comment-list .geren-kuang .kuang-shang .kuang-shang-1 .a {
        margin-top: 10px;
        font-size: 18px;
        font-weight: 700;
    }

    .note .post .comment-list .geren-kuang .kuang-shang .kuang-shang-1 .b {
        margin-top: 10px;
        font-size: 14px;
        margin-bottom: 20px;
    }

    .note .post .comment-list .geren-kuang .kuang-shang .kuang-shang-1 .c {
        margin-top: 6px;
        font-size: 13px;
        color: #999999;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-1 {
        width: 200px;
        height: 70px;
        float: left;
        display: block;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-1 .kuang-xia-1-1 {
        float: left;
        padding: 15px;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-1 .kuang-xia-1-1 .aa {
        font-weight: 700;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-1 .kuang-xia-1-1 p {
        padding: 0;
        margin: 0;
        text-align: center;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-2 .jianxin {
        display: inline-block;
        width: 90px;
        height: 40px;
        border: 1px solid green;
        border-radius: 20px;
        text-align: center;
        line-height: 40px;
        margin-top: 15px;
        margin-left: 20px;
        font-size: 15px;
        color: green!important;
    }

    .note .post .comment-list .geren-kuang .kuang-xia-2 .btn-success {
        display: inline-block;
        width: 100px;
        height: 40px;
        border-radius: 20px;
        text-align: center;
        line-height: 20px;
        margin-top: -5px;
        margin-left: 20px;
        color: white!important;
    }

    .note .post .comment-list .sanjiao {
        margin-top: 5px;
        margin-left: 210px;
        position: absolute;
        width: 15px;
        height: 15px;
        border-left: 1px solid #ccc;
        border-top: 1px solid #ccc;
        transform: rotate(225deg);
        background: white;
    }

    .note .post .comment-list .new-comment .avatar {
        position: absolute;
        left: -48px;
    }

    .note .post .comment-list .new-comment textarea {
        width: 100%;
        height: 80px;
        padding: 10px 15px;
        border: 1px solid #ccc;
        border-radius: 4px;
        display: inline-block;
        vertical-align: top;
        outline-style: none;
        resize: none;
        font-size: 13px;
        background: #f8f8f8;
    }

    .note .post .comment-list .new-comment .emoji-modal-wrap {
        position: relative;
    }

    .note .post .comment-list .new-comment .emoji {
        float: left;
        margin-top: 14px;
    }

    .note .post .comment-list .new-comment .emoji i {
        font-size: 20px;
        color: #969696;
    }

    .note .post .comment-list .new-comment .emoji i:hover {
        color: #333;
    }

    .note .post .comment-list .new-comment .hint {
        float: left;
        margin: 20px 0 0 20px;
        font-size: 13px;
        color: #969696;
    }

    .note .post .comment-list .new-comment .cancel {
        float: right;
        font-size: 16px;
        margin: 18px 30px 0 0;
        color: #969696!important;
    }

    .note .post .comment-list .new-comment .cancel:hover {
        color: #333!important;
    }

    .note .post .comment-list .new-comment .btn-send {
        float: right;
        width: 78px;
        padding: 8px 18px;
        margin: 10px 0;
        font-size: 18px;
        background: #42c02e;
        border-radius: 20px;
        color: #fff!important;
        box-shadow: none;
    }

    .note .post .comment-list .new-comment .btn-send:hover {
        background: #3db922;
    }

    .note .post .comment-list .new-comment .emoji-modal-wrap .emoji-modal {
        position: absolute;
        top: 50px;
        left: -48px;
        width: 402px;
        height: 208px;
        padding: 10px;
        border: 1px solid #d9d9d9;
        border-radius: 4px;
        box-shadow: 0 5px 25px rgba(0, 0, 0, 0.1);
        z-index: 1001;
    }

    .arrow-up:after {
        content: '';
        display: inline-block;
        position: absolute;
        left: 50px;
        top: -1px;
        width: 10px;
        height: 10px;
        border-left: 1px solid #aaa;
        border-top: 1px solid #aaa;
        transform: translate3d(0, -50%, 0) rotate(45deg);
        background: white;
    }

    .note .post .comment-list .normal-comment-list {
        margin-top: 30px;
    }

    .note .post .comment-list .top-title {
        padding-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
    }

    .note .post .comment-list .top-title span {
        font-size: 17px;
        font-weight: 700;
    }

    .note .post .comment-list .top-title .author-only {
        font-size: 12px;
        padding: 4px 8px;
        border: 1px solid #e1e1e1;
        border-radius: 12px;
        color: #969696!important;
        margin-left: 10px;
    }

    .note .post .comment-list .top-title .pull-right a {
        margin-left: 10px;
        font-size: 12px;
        color: #969696!important;
    }

    .note .post .comment-list .top-title .pull-right a.active {
        color: #2f2f2f!important;
    }

    .note .post .comment-list .comment {
        padding: 20px 0 30px 0;
        border-bottom: 1px solid #f0f0f0;
    }

    .note .post .comment-list .info {
        display: inline-block;
        vertical-align: middle;
    }

    .note .post .comment-list .info .name {
        font-size: 15px;
    }

    .note .post .comment-list .info .meta {
        font-size: 12px;
        color: #969696;
    }

    .note .post .comment-list .comment p {
        font-size: 16px;
        margin: 10px 0;
        line-height: 1.5;
        word-break: break-word!important;
    }

    .note .post .comment-list .comment .tool-group a {
        color: #969696!important;
        margin-right: 10px;
    }

    .note .post .comment-list .comment .tool-group a i {
        font-size: 18px;
        margin-right: 5px;
    }

    .note .post .comment-list .comment .tool-group .likeing i {
        background: #ea6f5a;
        color: #fff;
    }

    .note .post .comment-list .comment .tool-group a span {
        font-size: 14px;
    }

    .note .post .comment-list .sub-comment-list {
        border-left: 2px solid #d9d9d9;
        margin-top: 10px;
        padding: 0 0 0 20px;
    }

    .note .post .comment-list .sub-comment {
        padding-bottom: 15px;
        margin-bottom: 15px;
        border-bottom: 1px dashed #f0f0f0;
    }

    .note .post .comment-list .sub-comment p {
        font-size: 14px;
        line-height: 1.5;
        margin-bottom: 5px;
    }

    .note .post .comment-list .sub-comment p a {
        color: #3194d0!important;
    }

    .note .post .comment-list .sub-tool-group {
        font-size: 12px;
        color: #969696;
    }

    .note .post .comment-list .sub-tool-group a {
        margin-left: 10px;
    }

    .note .post .comment-list .sub-tool-group a i {
        margin-right: 5px;
    }

    .note .post .comment-list .more-comment {
        font-size: 14px;
        color: #969696;
    }

    .note .post .comment-list .more-comment a:hover {
        color: #333!important;
    }

    .note .post .comment-list .more-comment i {
        margin-right: 5px;
    }

    .note .post .comment-list .new-comment-1 {
        position: relative;
        margin-bottom: 20px;
    }

    .note .post .comment-list .new-comment-1 textarea {
        width: 100%;
        height: 80px;
        padding: 10px 15px;
        border: 1px solid #ccc;
        border-radius: 4px;
        display: inline-block;
        vertical-align: top;
        outline-style: none;
        resize: none;
        font-size: 13px;
        background: #f8f8f8;
    }

    .note .post .comment-list .new-comment-1 .emoji-modal-wrap {
        position: relative;
    }

    .note .post .comment-list .new-comment-1 .emoji {
        float: left;
        margin-top: 14px;
    }

    .note .post .comment-list .new-comment-1 .emoji i {
        font-size: 20px;
        color: #969696;
    }

    .note .post .comment-list .new-comment-1 .emoji i:hover {
        color: #333;
    }

    .note .post .comment-list .new-comment-1 .hint {
        float: left;
        margin: 20px 0 0 20px;
        font-size: 13px;
        color: #969696;
    }

    .note .post .comment-list .new-comment-1 .cancel {
        float: right;
        font-size: 16px;
        margin: 18px 30px 0 0;
        color: #969696!important;
    }

    .note .post .comment-list .new-comment-1 .cancel:hover {
        color: #333!important;
    }

    .note .post .comment-list .new-comment-1 .btn-send {
        float: right;
        width: 78px;
        padding: 8px 18px;
        margin: 10px 0;
        font-size: 18px;
        background: #42c02e;
        border-radius: 20px;
        color: #fff!important;
        box-shadow: none;
    }

    .note .post .comment-list .new-comment-1 .btn-send:hover {
        background: #3db922;
    }

    .note .post .comment-list .new-comment-1 .emoji-modal-wrap .emoji-modal {
        position: absolute;
        top: 50px;
        left: -48px;
        width: 402px;
        height: 208px;
        padding: 10px;
        border: 1px solid #d9d9d9;
        border-radius: 4px;
        box-shadow: 0 5px 25px rgba(0, 0, 0, 0.1);
        z-index: 1001;
        background: white;
    }
</style>