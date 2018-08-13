<template>
  <div>
      <h2>News Index page</h2>
      <p>NewsID:{{$route.params.newsId}}</p>
      <ul>
        <li><nuxt-link :to="{name: 'index'}">home</nuxt-link></li>

        <!-- 动画效果需要 nuxt-link 配合,否则无效 -->
        <li><nuxt-link :to="{name:'news-id',params:{id:123,title:'fri'}}">News-1</nuxt-link></li>
      </ul>
     
  </div>
</template>

<script type='text/ecmascript-6'>
export default {
  name: 'name',
  data() {
    return {
      id: [1,2,3,4,5,6]
    }
  }
  
}
</script>
<style scoped>

</style>
