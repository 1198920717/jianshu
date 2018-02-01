<template>
    <div>
        <my-header></my-header>
        <div class="note">
            <!-- 文章区域 -->
            <div class="post">
                <!-- 正文 -->
                <div class="article">
                    <h1 class="title">月薪三千，就该去死吗？</h1>
                    <div class="author">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../../assets/img/default.avatar.jpg" alt="">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>

                            <a class="btn-sm" href="javascript:void(0);" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                                <i class="fa" :class="iconObj" ref="icon"></i>
                                <span ref="followWord">关注</span>
                            </a>
                            <div class="meta">
                                <span>2018.01.23 16:09</span>
                                <span>字数 2273</span>
                                <span>阅读 882</span>
                                <span>评论 7</span>
                                <span>喜欢 34</span>
                            </div>
                        </div>
                    </div>
                    <!-- 文章内容 -->
                    <div class="show-content">
                        <p>01</p>
                        <p>失眠的原因是看了电影《无问西东》，其中一个场景久久地萦绕于脑中：</p>
                        <p>吴岭澜是影中一位文学天赋极高但理科极差的学生。对于人生，他很少思考过，一味地随着大众的价值认知漂流。</p>
                        <p>当校长梅贻琦问他：“为什么不转去文学系？”时，他这样回答道：</p>
                        <p>“ 最好的学生都是学实科的。我只知道，这个年纪最重要的就是学习，何用管我学什么。每天把自己交给书本，心里就觉得踏实。”</p>
                        <p>梅贻琦答他：</p>
                        <p>“ 你还忽略了一件事，真实。人把自己置身于忙碌当中，有一种麻木的踏实，但丧失了真实。”</p>
                        <p>“什么是真实？”</p>
                        <p>“ 真实就是，你看什么，做什么，和谁在一起，有一种从心灵深处满溢出来的不懊悔、也不羞耻的平和与喜悦。”</p>
                        <p>真实已经离我们多数人很远很远。不知从什么时候开始，“人生在世，名利二字”已经成为我们做人做事的行为标准，理想成为了一个人可以被嘲笑的代言词。若是一个人谈对他人的价值、对社会的奉献恐怕又会被扣上一顶“鸡汤”或“忽悠”的帽子。</p>
                        <p>做不了真实的自己，表达不了真实的自己，我们将原因归咎于现实。</p>
                        <p>“想法很美好，但现实是...”这种句调的语气成了多数人的常用句式。</p>
                        <p>02</p>
                        <p>在前年练习运营社群时，我在网上结识了一位比较厉害的牛人，他跟我们同龄，但不同的是人家现在已经工作了。</p>
                        <p>在一次聊天中，我就人生设计这个话题咨询了他，他跟我聊了聊他目前为止的人生经历：</p>
                        <p>家在上海，从小在美国长大念书，耶鲁大学本科毕业，修学金融和经济双学位，大学期间进入摩根士丹利和麦肯锡公司实习，成绩优异获得保研资格，除此之外人家业余时间还是专业模特，考国际驾照，赛车手。</p>
                        <p>还有一项，他特别向我强调，一年读200多本书。</p>
                        <p>我很惊讶，便问：“这些是从你十五六岁就开始规划的吗？”</p>
                        <p>他回答道：“不，还要早，从12岁就开始了。”</p>
                        <p>人生是需要设计的，需要家族的积累和指点，多数人在大学感到迷茫的原因，是因为缺少必要的人生设计和规划。</p>
                        <p>上大学之前，我们就一件事情：参加高考，人生被精确到小时的课程安排的满满当当。</p>
                        <p>上大学后，脱离了老师的束缚，大部分家长也开始懈怠，对个人的要求降低，自己也会不由自觉地放松。有时候会出现这种情况：你很想努力上进，但不知道要做什么。</p>
                        <p>堕落都是一步一步的，你挣扎过、探索过，然而对于每一件事，没有人告诉你它的价值和意义所在，孰重孰轻你拎不清，等明白了，也往往晚了，同样的事情只能由自己的下一代去重视和完成。</p>
                        <p>还有种情况：你知道要做什么，但不知道怎么去做。</p>
                        <p>你投身学业，刻苦努力，但考出的成绩总是比不上那些你身边更有天资的同学。你知道要努力，但你不知道比努力更重要的是，他们选择这个专业是有计划的，他们热爱这门学问，而热爱，才是高分的关键秘诀。</p>
                        <p>而那些越是父母受教育程度高、经济实力越强的家庭，为孩子未来的人生发展规划能规划出最优化最高效的路线，让他早日摆脱“现实”的束缚进而追求“真实”，境由心转，有更多时间思考自己想过的生活，有更多精力实现自己的价值。</p>
                        <p>03</p>
                        <p>凛冬已至，暴雪纷飞，在一次聚餐聊天中我了解到一位朋友正面临的巨大选择压力。</p>
                        <p>他现在在东北上大学，一次偶然的机会，他报名了飞行员测试并成功通过。他正在跟航空公司谈签约事宜。</p>
                        <p>做飞行员，优势在于工作有保障，年薪高，自由时间长，退休早；劣势也很明显，一签就是几十年，意味着终身从事这种行业，并且要求随叫随到，生活没有固定的节奏，离家太远，不能及时照顾父母等等。</p>
                        <p>他在纠结，到底是选择去南方的城市自己打拼还是过飞行员这种生活。</p>
                        <p>这个问题本质上是要不要用自由来换取资源。对于普通人来说，自己打拼是个很辛苦很艰难的过程，面临着巨大的不确定性，一旦失败就得告老还乡。</p>
                        <p>这也是我们多数普通人面临的困境，一方面想为真实的自己留出时间和精力，另一方面又要为现实的生活而纠结徘徊。</p>
                        <p>在家和父母聊天时，他们问我：“你将来想做什么？”我想都没想地回答道：“做什么从事哪个职业不重要，重要的是做什么能帮助我实现财务自由，让我从繁重的日常琐事中抽身出来，那时再去追求自己想要的生活。”</p>
                        <p>在你做自己想做的事情之前，你需要做一些自己不喜欢做的事。高考，雅思，托福，拼命背书学习，求职加薪，这些对普通人来说，都是通向真实的自己的有力步骤。</p>
                        <p>但悲哀的一点就在于，许多人把这些东西当做了追求的目的地，而不是沿途的风景。我们最终的目的地，远不止在功利。</p>
                        <p>04</p>
                        <p>“我在你们这个年纪，有段时间，远离人群，独自思索，我的人生到底应该怎样度过...”</p>
                        <p>电影中的这句话简直是我现在生活的写照。</p>
                        <p>由于交流的缘故，我离开了原学校，到了一个全新的陌生的环境，没有复杂的人际关系，没有应酬的活动，宿舍也只有4个人。</p>
                        <p>客观环境为我营造了一种被逼无奈思考自身前途命运的氛围。那一年，我真的像电影中所说的这样，对“人生到底该怎样度过”的问题思考到头脑发疼。</p>
                        <p>就算我20出头开始发愤图强，拼搏几十年实现财务自由，获得一定社会地位后，那样的生活真的是我想要的吗？</p>
                        <p>我要到哪里去，要去帮助哪些人，要如何去探寻自己真实的生命体验，我不想再一次后悔，过一种毫无波澜和没有亮点的人生。</p>
                        <p>在漫漫长夜中，我想到了一个曾经很鄙弃的词：“理想。”</p>
                        <p>突然发现，有理想的人才是最有力量的，他们得经过多少日日夜夜的苦苦思索，才找到自己这个人生的终极目的，并为之奋斗一生，每一次呼吸，每一个成功或失败，他们真实地过完自己生命中的每一天，快乐、踏实而又心安理得。</p>
                        <p>不得不承认，现在这个词不仅离我，还有许许多多的大学生都很远很远。名利是刚需，但它仅仅是手段而非目的本身，在理想奋斗道路上的人生本身已不平庸。</p>
                        <p>在我即将离开的最后一天，我的室友送我了一本书作为离别礼物。</p>
                    </div>
                    <div class="show-foot">
                        <nuxt-link to="/nb/123" class="notebook">
                            <i class="fa fa-book"></i>
                            <span>我的文集</span>
                        </nuxt-link>
                        <div class="copyright">
                            © 著作权归作者所有
                        </div>
                    </div>
                    <div class="follow-detail">
                        <div class="info">
                            <nuxt-link to="/u/123" class="avatar">
                                <img src="../../assets/img/default.avatar.jpg" alt="">
                            </nuxt-link>
                            <a href="javascript:void(0);" class="btn btn-success" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                                <i class="fa" :class="iconObj" ref="icon2"></i>
                                <span ref="followWord2">关注</span>
                            </a>
                            <nuxt-link to="/u/123" class="title">
                                测试用户
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                            <p>写了 343608 字，被 43223 人关注，获得了 39700 个喜欢</p>
                        </div>
                        <div class="signature">
                            2018，田宝与你共同成长。 专注于自媒体写作，读书方法，时间管理，学习心得。
                        </div>
                    </div>
                    <div class="meta-bottom">
                        <div class="like">
                            <div class="btn like-group" :class="likeObj" @click="like1">
                                <div class="btn-like">
                                    <a href="javascript:void(0);">
                                        <i class="fa fa-heart-o"></i>
                                        <span>喜欢</span>
                                    </a>
                                </div>
                                <div class="modal-wrap">
                                    <a ref="a">34</a>
                                </div>
                            </div>
                        </div>
                        <div class="share-group">

                            <a href="javascript:void(0);" @mouseover="aaa=true" @mouseleave="aaa=false">
                                <div class="hahaha1" v-show="aaa">
                                    <div class="sanjiao"></div>
                                    <span>分享到微博</span>
                                </div>

                                <i class="fa fa-weibo weibo"></i>
                            </a>
                            <a href="javascript:void(0);" @mouseover="bbb=true" @mouseleave="bbb=false">
                                <div class="hahaha2" v-show="bbb">
                                    <div class="sanjiao"></div>
                                    <span>分享到微信</span>
                                </div>
                                <i class="fa fa-weixin weixin"></i>
                            </a>
                            <a href="javascript:void(0);" @mouseover="ccc=true" @mouseleave="ccc=false">
                                <div class="hahaha3" v-show="ccc">
                                    <div class="sanjiao"></div>
                                    <span>分享到QQ</span>
                                </div>
                                <i class="fa fa-qq qq"></i>
                            </a>
                            <a href="javascript:void(0);" class="more-share" @mouseover="ddd=true" @mouseleave="ddd=false">
                                <div class="gengduo" v-show="ddd">
                                    <div class="sanjiao1"></div>
                                    <div href="" class="gengduo-1">
                                        <i class="fa fa-star-o "></i>
                                        <span>分享到QQ空间</span>
                                    </div>
                                    <div href="" class="gengduo-1">
                                        <i class="fa fa-signing "></i>
                                        <span>分享到Twitter</span>
                                    </div>
                                    <div href="" class="gengduo-1">
                                        <i class="fa fa-share-square"></i>
                                        <span>分享到Facebook</span>
                                    </div>
                                    <div href="" class="gengduo-1">
                                        <i class="fa fa-hand-pointer-o "></i>
                                        <span>分享到Google+</span>
                                    </div>
                                    <div href="" class="gengduo-1">
                                        <i class="fa fa-header "></i>
                                        <span>分享到豆瓣</span>
                                    </div>
                                </div>
                                更多分享
                            </a>
                        </div>

                    </div>
                </div>
                <!-- 回复组件 -->
                <my-comment></my-comment>
            </div>
            <!-- 悬浮的操作框 -->
            <div class="side-bar"></div>
            <!-- 对应的推荐阅读 -->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../../components/myHeader.vue'
    import myComment from '../../components/myComment.vue'
    export default {
        data() {
            return {
                followObj: {
                    'follow': true,
                    'following': false
                },
                iconObj: {
                    'fa-plus-square-o': true,
                    'fa-check': false
                },
                likeObj: {
                    'like': true,
                    'likeing': false
                },
                aaa: false,
                bbb: false,
                ccc: false,
                ddd: false
            }
        },
        components: {
            myHeader,
            myComment
        },
        methods: {
            isFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                // 这里预留ajax的操作
                this.followObj.follow = !this.followObj.follow;
                this.followObj.following = !this.followObj.following;
                this.iconObj['fa-plus-square-o'] = !this.iconObj['fa-plus-square-o'];
                this.iconObj['fa-check'] = !this.iconObj['fa-check'];
                this.$refs.followWord.innerHTML = word == '关注' ? '已关注' : '关注';
                this.$refs.followWord2.innerHTML = word == '关注' ? '已关注' : '关注';
            },
            noFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '已关注') {
                    this.$refs.followWord.innerHTML = '取消关注';
                    this.$refs.icon.className = 'fa fa-close';
                    this.$refs.followWord2.innerHTML = '取消关注';
                    this.$refs.icon2.className = 'fa fa-close';
                }
            },
            beFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '取消关注') {
                    this.$refs.followWord.innerHTML = '已关注';
                    this.$refs.icon.className = 'fa fa-check';
                    this.$refs.followWord2.innerHTML = '已关注';
                    this.$refs.icon2.className = 'fa fa-check';
                }
            },
            like1: function () {
                let word = this.$refs.a.innerHTML;
                this.likeObj.like = !this.likeObj.like;
                this.likeObj.likeing = !this.likeObj.likeing;
                this.$refs.a.innerHTML = word == '34' ? '35' : '34';
            }

        }
    }   
</script>