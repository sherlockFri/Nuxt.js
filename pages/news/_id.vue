<template>
  <div>
      <h2>News-Content [{{$route.params.id}}]</h2>
      <ul>
        <li><a href="/">Home</a></li>
      </ul>

  </div>
</template>
<script>
 

  export default {
    // 动态参数校验,参数正确调正常页面,不正确调 404 页面
    validate ({ params }) {
      // Must be a number
      return /^\d+$/.test(params.id)
    },

    data(){
      return{
        title:this.$route.params.title,
      }
    },
  
    //独立设置head信息
    head(){
      return{
        title:this.title,
        meta:[

          //为了避免子组件中的meta标签不能正确覆盖父组件中相同的标签而产生重复的现象，
          //建议利用 hid 键为meta标签配一个唯一的标识编号。
          {hid:'description',name:'news',content:'This is news page'}
        ]
      }
    }
  }
</script>>
