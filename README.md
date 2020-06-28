## react-cli
> 从0配置react-cli，毛胚架子之后关于react的项目以这个为出发点，已经用yarn锁版本号。
#### 安装插件
1. react react-dom
2. babel-loader@7.x
3. babel-core babel-plugin-transform-runtime babel-polyfill babel-preset-env babel-preset-react
4. html-loader
5. html-webpack-plugin
6. ···自己看package.json

#### 配置webpack
配置好入口/出口/插件/加载器， 具体的看webpack.config.js

#### .babelrc
babel是js的语法编译器。在bable6.x版本以后，所有的插件都是可插拔的，也就是说只是安装babel是无法正常工作的，必须配置.bashrc文件才能起作用配置的时候注意两项预设(presets)和插件(plugins)。

1. preset

作用是为babel安装特定的插件，比如现在作用的env和react

2. plugins

 presets是插件plugins的预设，也就是说直接需要不需要的插件一起引入，如果不想使用presets，可以单独使用plugins对某个功能进行单独的引入。一些方法是preset不提供的，那么我们就需要plugins，比如我们用到的transform-runtime：解决编译中产生的重复的工具函数，减小代码体积。