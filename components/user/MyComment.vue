<template>
    <div>
        <ul class="note-list">
            <li>
                <div class="content">
                    <div class="author">
                        <nuxt-link to="/u/123" class="avatar">
                            <img src="~assets/img/default-avatar.jpg">
                        </nuxt-link>
                        <div class="info">
                            <nuxt-link to="/u/123" class="nickname">简宝玉</nuxt-link>
                            <span class="time">5分钟前</span>
                        </div>
                    </div>
                    <nuxt-link class="title" to="/p/123">
                        男人是可以被改变的生物
                    </nuxt-link>
                    <p class="abstract">

                        翻看以前她发的那些朋友圈，不是“女人要自立自强”就是“男人要是靠的住，母猪都能上树去”的话，再就是晒自己的娃，今天学跳舞明天学画画。
                        对于后者，我是一名宝妈，我很是理解，自己家的闺女，优秀的地方晒晒无可厚非。对于前者的做法，我不太赞同，或许家里的那位真的不太靠谱，
                        不过照她这个整天批评的口气，她丈夫即便想靠谱下，看到朋友圈妻子这样的评价后，也会偃旗息鼓。
                    </p>
                    <div class="meta">
                        <nuxt-link class="tag" to="/p/123">
                            <i class="fa fa-eye"></i>
                            100
                        </nuxt-link>
                        <nuxt-link class="tag" to="/p/123">
                            <i class="fa fa-comment"></i>
                            200
                        </nuxt-link>
                        <span>
                            <i class="fa fa-heart"></i>
                            15
                        </span>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        name: "MyComment"
    }
</script>