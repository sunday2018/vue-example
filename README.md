# VUE
轻量级MVVM框架
使用数据驱动+组件化开发
数据双向绑定（修改视图时数据也会赋值给model，更改model时也会反应到视图上。）

## vue学习小实例
basic_application vue基础应用，纯语法示例


## VUE技术栈
1. npm 包管理工具。
2. ES6 javascript的新版本，可以简化js代码，同时利用其提供的强大功能快速实现JS逻辑。
2. vue-cli vue的脚手架工具，用于自动生成vue项目的目录及文件。
3. vue-router 前段路由工具，利用页面的路由控制、局部刷新及按需加载，构建单页应用，实现前后端分离。
4. webpack 强大的文件打包工具，将前段项目距文件统一打包压缩至js中，并且可以通过vue-loader等加载器实现语法转化与加载。


## webpack
### 安装
npm init
(切换到项目根目录，安装到项目目录中，生成node_moudules目录和package-lock.json文件)
npm install --save-dev webpack

### 打包
webpack <源文件> -o <目标文件>
(npm install webpack-cli -g)


## vue脚手架初始化项目
环境准备工作：
1. 安装cnpm
npm install -g cnpm --registry=https://registry.npm.taobao.org
2. 安装vue, vue-router
npm install vue
npm install vue-router
3. 安装vue-cli
npm install @vue/cli
4. 检测vue-cli是否安装成功
vue -V
5. 查看webpack
webpack -v

构建项目：
1. 在工作目录下新建一个vue项目
vue init webpack <project_name>
（<project_name>目录会自动创建，若已手动创建，需cd的此目录下执行vue init webpack）
目录解释说明：
build 最终发布的代码的存放位置
config 配置路径、端口号等一些信息
node_modules npm加载的项目所需要的各种依赖模块
src 源码目录
  assets 存放图片
  components 组件文件
  router/index.js 路由配置
  App.vue 羡慕入口组件
  main.js 项目核心文件（整个项目的入口js），引入依赖包、默认页面样式等（项目运行后回在index.html中形成一个app.js文件）。
static 静态资源目录，如图片、字体等
test 初始测试目录
index.html 单页面入口文件
package.json 项目配置信息文件/所依赖的开发博的版本信息及所依赖的插件信息
README.md 项目说明文件
webpack.config.js webpack的位置文件
。babelrc 检测es6语法的文件配置
.getignore 忽略文件的配置
.postcssrc.js 前缀的配置

2. 运行vue项目
npm run dev
3. 浏览器访问localhost:8080
4. 安装element-ui
npm i element-ui -S
5. 在src/main.js中引用element-ui



## npm包管理器命令
npm 集成在node.js中
npm install -g cnpm --registry=http://registry.npm.taobao.org

npm 切换镜像：npm config set registry https://registry.npm.taobao.org
验证镜像源： npm config get registry