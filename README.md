# VUE
![VUE](https://github.com/sunday2018/myMarkdownImage/blob/master/vue.png)
* 轻量级MVVM框架
* 使用数据驱动+组件化开发
* 数据双向绑定（修改视图时数据也会赋值给model，更改model时也会反应到视图上。）

## 目录说明
* ***basic-application*** vue基础应用，属于纯语法示例。
* ***vue-element*** vue-cli脚手架项目，并集成element。


## VUE技术栈
1. ***npm*** 包管理工具。
2. ***ES6*** javascript的新版本，可以简化js代码，同时利用其提供的强大功能快速实现JS逻辑。
2. ***vue-cli*** vue的脚手架工具，用于自动生成vue项目的目录及文件。
3. ***vue-router*** 前段路由工具，利用页面的路由控制、局部刷新及按需加载，构建单页应用，实现前后端分离。
4. ***webpack*** 强大的文件打包工具，将前段项目距文件统一打包压缩至js中，并且可以通过vue-loader等加载器实现语法转化与加载。


## 环境搭建
1. 安装webpack  
```npm init```  
(切换到项目根目录，安装到项目目录中，生成node_moudules目录和package-lock.json文件)  
```npm install --save-dev webpack```  
全局安装：```npm install -g webpack```
2. 安装cnpm  
```npm install -g cnpm --registry=https://registry.npm.taobao.org```
3. 安装vue, vue-router  
```npm install vue```  
```npm install vue-router```
4. 安装vue-cli
```npm install -g @vue/cli```  
	检测vue-cli是否安装成功  
```vue -V```

## 构建并运行项目
1. 使用vue-cli脚手架构建项目 ```vue init webpack <project_name>```
2. ```cd <project_name>```
3. 安装依赖包：```npm install```
4. 开发模式下运行程序：```npm run dev```
5. 浏览器访问：http://127.0.0.1:8080
6. 服务器打包部署：```npm run build```
7. 根目录形成dist文件夹，此目录下的内容即为上传到服务器上的文件

## 集成element
* 安装element-ui
	1. 切换到项目根目录：```cd <project root path>```
	2. 安装element-ui
	```npm i element-ui -g```  
	> 安装后package.json中的dependencies会增加element-ui依赖
	3. ```cnpm i element-ui -S```
* 在main.js中配置element-ui
在main.js中增加导入和让VUE使用elementUI  
```
import Vue from 'vue'
import App from './App'
import router from './router'

import ElementUI from 'element-ui'

Vue.config.productionTip = false

Vue.use(ElementUI)

new Vue({
	el: '#app',
	router,
	componsents: { App },
	template: '<App/>'
	})
```
* 安装依赖
npm install
* 使用element-ui
创建文件helloWrold.vue
```

```



## npm包管理器命令
安装cnpm：```npm install -g cnpm --registry=http://registry.npm.taobao.org```  
npm切换镜像：```npm config set registry https://registry.npm.taobao.org```  
验证镜像源： ```npm config get registry```  
清除缓存：```npm cache clean --fource```  
