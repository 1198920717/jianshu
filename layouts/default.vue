<template>
  <div>
    <nuxt/>
  </div>
</template>
<script>
import vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
vue.use(BootstrapVue);
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  layout:'sign',//指明当前页面所使用的默认模板是layouts文件夹下的sign.vue
}
</script>
