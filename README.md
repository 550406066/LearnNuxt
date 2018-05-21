# learn-nuxt

> Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).
##安装nuxt
$ vue init nuxt/starter 项目名
![安装项目](https://i.imgur.com/lJOMLN0.png)
>要求node>8.0.0
之后在项目中安装即可  

##下图为初始化页面：  

![初始化页面](https://i.imgur.com/IsdSkRI.png)

##目录内容
|-- .nuxt                            // Nuxt自动生成，临时的用于编辑的文件，build  

|-- assets                           // 用于组织未编译的静态资源入LESS、SASS 或 JavaScript  

|-- components                       // 用于自己编写的Vue组件，比如滚动组件，日历组件，分页组件  

|-- layouts                          // 布局目录，用于组织应用的布局组件，不可更改。  

|-- middleware                       // 用于存放中间件  

|-- pages                            // 用于存放写的页面，我们主要的工作区域  

|-- plugins                          // 用于存放JavaScript插件的地方  

|-- static                           // 用于存放静态资源文件，比如图片  

|-- store                            // 用于组织应用的Vuex 状态管理。  

|-- .editorconfig                    // 开发工具格式配置  

|-- .eslintrc.js                     // ESLint的配置文件，用于检查代码格式  

|-- .gitignore                       // 配置git不上传的文件  

|-- nuxt.config.json                 // 用于组织Nuxt.js应用的个性化配置，已覆盖默认配置  

|-- package-lock.json                // npm自动生成，用于帮助package的统一性设置的，yarn也有相同的操作  

|-- package-lock.json                // npm自动生成，用于帮助package的统一性设置的，yarn也有相同的操作  

|-- package.json                     // npm包管理配置文件 
##常用配置
>修改端口：在根目录下的package.json修改

![修改端口配置](https://i.imgur.com/aFO7lJ1.png)

>添加全局css：在assets目录下的新建css/normailze.css

>引用:在根目录的nuxt.congig.js下添加

* css:['~assets/css/normailze.css'],


##路由配置
>nuxt会**自动**根据目录进行页面路由配置，也就是说我们只需在pages目录下新建对应的路由便可使用下面语句跳转到对应页面

  `<nuxt-link :to="{name:'about'}">HOME</nuxt-link>`

###页面如下：
![路由配置](https://i.imgur.com/WaHDVpi.png)

传递参数和vue-router相同

####query和params以<nuxt-link>打开的区别：

* query会在路由中显示
* params不会在路由中显示，**刷新后丢失！**

###动态路由：
>路由部分和vue-router一样不过路由匹配是新建以_开头的文件，这个文件名就是匹配到的动态路由的值。校验使用nuxt提供的validate方法。


![动态路由](https://i.imgur.com/Jnn4mLz.png)

>![匹配动态路由](https://i.imgur.com/pJ7rr3F.png)

##默认模板
在根目录下新建app.html后写入下图内容，之后**重新启动服务**
![添加模板](https://i.imgur.com/OSOZuXT.png)
>而layouts下的default.vue相当于vue中的app.vue在其中添加内容也可以实现模板的功能
![添加模板](https://i.imgur.com/Y1tbEOE.png)

##设置meta
>meta中的hid是标识符，设置和原来nuxt.config.js相同便可替代默认的meta

![设置meta](https://i.imgur.com/yImUh0d.png)
##使用axios
nuxt使用asyncData扩展了vue之后点击会再次请求新的数据

![获取后端数据](https://i.imgur.com/EJBgghm.png)

#官方地址
https://zh.nuxtjs.org/guide/async-data