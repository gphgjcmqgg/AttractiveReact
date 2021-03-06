# AttractiveReact

前端react开发学习
诱人的React

## bootcdn 稳定、快速、免费的前端开源项目 CDN 加速服务

https://www.bootcdn.cn/

## babel

把react jsx语法转换成js语法

## create-react-app 官方推荐脚手架

开发 react 应用最好用的脚手架 create-react-app,facebook官方开发
安装create-react-app脚手架

1. npm install -g create-react-app
2. create-react-app hello-react
3. yarn start | yarn build
4. yarn global add serve | serve -s build
5. yarn run eject 运行后可以进行自定义配置

类似这样的脚手架，我扫了网络上比较多人用和关注的，一共发现了三个

1. react-boilerplate
2. react-redux-starter-kit
3. create-react-app

### create-react-app 特点

1. 简单的安装使用
2. 源码结构简单清晰
3. 线上编译命令
4. api开发
开发环境中，你的react应用是跑在3000端口的，可是api服务可能跑在3001端口，这个时候，你跟api服务器交互的时候，可能会使用fetch或各种请求库，比如jquery的ajax。

这个时候可能会遇到CORS问题，毕竟端口不同，而线上环境却没有这个问题，因为你都控制线上环境的react应用和api应用，跑在同一个端口上。
开发环境可以使用代理： 解决CORS问题 "proxy": "http://localhost:3001/"

## npm 和 yarn 切换淘宝镜像

```
npm config set registry https://registry.npm.taobao.org
yarn config set registry https://registry.npm.taobao.org
```
## react组件创建方式

1. createClass
2. class X extends React.Component
3. const X = (props) => { return (......)}
创建函数式组件（无状态组件）
1）无需state，即不处理用户的输入，组件的所有的数据都是依赖props传入的
2）不需要用到生命周期函数
好处
1）不需要声明类，可以避免大量的譬如extends或者constructor这样的代码
2）不需要显示声明this关键字，在ES6的类声明中往往需要将函数的this关键字绑定到当前作用域，而因为函数式声明的特性，我们不需要再强制绑定

## react组件间传值

父组件给子组件传递参数是通过props（向下传递）
子组件给父组件传递参数是通过父组件提供的回调函数（向上传递）