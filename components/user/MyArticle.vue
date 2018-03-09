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
                        谈恋爱，你走心还是走肾？
                    </nuxt-link>
                    <p class="abstract">

                        恋爱，也许是男女之最浪漫的事了。 
                        的确，恋爱让人欲仙欲死，牵肠挂肚。 
                        恋爱，让人觉得生命短暂，人生无限美好。 
                        恋爱，让人诗情大发，才高八斗。 一个人一生没谈过恋爱的话，真是枉来人世走一回。 
                        一个人如果没经过一次恋爱的洗礼，那还真不知道人生之爱为何物，男女关系欲为何？
                        恋爱，有爱才会恋，有恋才会梦里相思人憔悴。只有爱入骨髓，才会食不知味，夜不能寐，随时随地肯相陪。 
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
        name: "MyArticle"
    }
</script>