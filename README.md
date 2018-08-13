# 1.package.json配置,改变默认地址
   "config":{
    "nuxt":{
      "host":"127.0.0.1",
      "port":"1818"
    }
  },
# 1.1 nuxt.config.js配置全局的css normalize.css

# 2.路由配置用 <nuxt-link> 标签 代替 a
# 2.1路径和传参为<nuxt :to="{name: '文件夹名字', params: {参数名称: 参数}}">
# 2.2 动态路由组件以通文件夹下以下划线_开头的文件,如_id.vue

# 3.1 配置全局页面的css动画,在nuxt.config.js 加上css:['assets/css/main.css'],编辑动画
# 3.2 配置独立的动画,在assets/css/main.css编辑动画然后再组件引入

# 4.1 默认模板根目录下创建一个app.html,建立默认模板必须重启!!!

# 5.1错误页面指引,在根目录下的layouts文件夹下建立一个error.vue文件
# 5.2个性meta设置,/pages/news/_id.vue增加head 配置

# 6.1 asyncData(), 新增方法, 获取数据,pages下建asyncData.vue