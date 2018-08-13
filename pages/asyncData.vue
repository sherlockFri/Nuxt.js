<template>
  <div>
      <h1>姓名：{{info.name}}</h1>
      <h2>年龄：{{info.age}}</h2>
      <h2>兴趣：{{info.interest}}</h2>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  data(){
     return {
         name:'hello World',
     }
  },
  // asyncData(){
  //     return axios.get('https://api.myjson.com/bins/1da45o')
  //     .then((res)=>{
  //         console.log(res)
  //         return {info:res.data}
  //     })
      
  // }

  // async...awati 方法 获取数据
  async asyncData(){
      let {data} = await axios.get('https://api.myjson.com/bins/1da45o')
      return {info: data}
  }
}
</script>