# **Vue使用指南**

> 一套用于构建用户界面的渐进式JavaScript框架

## **配置开发环境**

**Vue分为开发版与生产版，在vue.js文件中可以更改vue配置。**



### 关闭浏览器对使用开发版本的警告

Vue.config.productionTip

- **类型**：`boolean`

- **默认值**：`true`

- **用法**：

  设置为 `false` 以阻止 vue 在启动时生成生产提示。



### 网页图标请求

- 浏览器打开时会自动像服务器请求favicon.ico文件
- favicon.ico文件作为浏览器页面标题的小图标呈现

![image-20221110162702772](../../picture_typora/Vue使用指南/image-20221110162702772.png)





## Vue程序

<img src="../../picture_typora/Vue使用指南/image-20221110215601012.png" style:room="80%">



### Hello_Vue



### 计数器

![image-20230224001050221](../../picture_typora/Vue使用指南/image-20230224001050221.png)

```vue
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<div id="app">
    <h2>当前计数为：{{counter}}</h2>
    <button v-on:click="add">+</button>
    <!-- 语法糖：@click是v-on:click的简写 -->
    <button @click="counter--">-</button>
</div>
<script src="../js/vue.js"></script>
<script>
    let app=new Vue({
        el:'#app',
        data:{
            counter:0
        },
        methods:{
            add: function (){
                console.log('add被执行');
                this.counter++
            }
        }
    })
</script>
</body>
</html>
```





## MVVM

![image-20230225133214074](../../picture_typora/Vue使用指南/image-20230225133214074.png)

> MVVM有助于将[图形用户界面](https://zh.wikipedia.org/wiki/图形用户界面)的开发与[业务逻辑](https://zh.wikipedia.org/wiki/业务逻辑)或[后端](https://zh.wikipedia.org/wiki/前端和后端)逻辑（*数据模型*）的开发[分离](https://zh.wikipedia.org/wiki/关注点分离)开来，这是通过[置标语言](https://zh.wikipedia.org/wiki/置标语言)或GUI代码实现的。MVVM的*视图模型*是一个值转换器，[[1\]](https://zh.wikipedia.org/zh-cn/MVVM#cite_note-MVVM-eliminates-valueconverters-1) 这意味着视图模型负责从模型中暴露（转换）[数据对象](https://zh.wikipedia.org/wiki/对象_(计算机科学))，以便轻松管理和呈现对象。在这方面，视图模型比视图做得更多，并且处理大部分视图的显示逻辑。[[1\]](https://zh.wikipedia.org/zh-cn/MVVM#cite_note-MVVM-eliminates-valueconverters-1) 视图模型可以实现[中介者模式](https://zh.wikipedia.org/wiki/中介者模式)，组织对视图所支持的[用例](https://zh.wikipedia.org/wiki/用例)集的后端逻辑的访问。

<img src="../../picture_typora/Vue使用指南/image-20230225133554949.png" alt="image-20230225133554949" style="zoom:80%;" />



## Vue的生命周期

- 
