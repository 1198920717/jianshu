<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <img class="tag-banner" src="../assets/img/收藏的文章.png" alt="">
                    <div id="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic.jpg" alt="">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/logo.png">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="" class="nickname">
                                                测试用户
                                            </nuxt-link>
                                            <span class="time">02.16 20:45</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同， 于是市场上出现很多读书方法，比如速度、多读、慢读、列读…… 不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">  
                                        <nuxt-link class="" to="/p/123">
                                            <i class="fa fa-eye"></i>
                                            579
                                        </nuxt-link>
                                        <nuxt-link to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            200
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            546
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '../components/myHeader'
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
    .tag-banner {
        margin-bottom: 30px;
    }

    .tag-banner {
        width: 100%;
        min-height: 100px;
        background-color: hsla(0, 0%, 71%, .2);
        border-radius: 6px;
    }

    .col-8 {
        max-width: 75%;
        margin-left: 12.5%;
    }
    .meta span{
        font-size: 13px;
    }
</style>