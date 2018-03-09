<template>
    <div>
        <ul class="user-list" infinite-scroll-url="/users/9a6682699277/following" data-placeholder="user">
            <li>
                <a class="avatar" href="/u/7406f22f461e">
                    <img src="//upload.jianshu.io/users/upload_avatars/3090078/f1cdcde073ec.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180"
                        alt="180">
                </a>
                <div class="info">
                    <a class="name" href="/u/7406f22f461e">雨落荒原</a>
                    <i class="iconfont ic-woman"></i>
                    <div class="meta">
                        <span>关注 88</span>
                        <span>粉丝 9977</span>
                        <span>文章 30</span>
                    </div>
                    <div class="meta">
                        写了 125893 字，获得了 813 个喜欢
                    </div>
                </div>
                <a class="btn btn-default following">
                    <i class="fa fa-check"></i>
                    <span>已关注</span>
                </a>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        name: "guanzhu"
    }
</script>
<style scoped>
.btn-default{
    border: 1px solid #bbb;
    border-radius: 30px;
    color: #888!important;
    background-color:white!important; 
}
</style>