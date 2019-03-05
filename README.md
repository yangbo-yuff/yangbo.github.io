#一. 回顾
经过前面几个笔记，环境的配置，相关依赖的安装，以及IDE的选择，我们基本上已经做好开发React Nativexian项目的准备了。

在正式开发前，我们还需要了解React Nativexian项目的项目结构，这样会让我们的开发更得心应手。

#二. 项目结构分析
##1. 项目结构
我们还是拿之前新建的项目来折腾，在终端执行以下
```
cd  YangBoProject
code .
```
打开项目我们会看到下图所示的项目结构

![项目结构](https://upload-images.jianshu.io/upload_images/12972541-a786935e59fd2dac.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##2. 结构描述

React Native结构描述
  |                 名称	               |                描述 |
| :-------: |:-------------:|
|  \_tests\_   |  测试文件夹，执行命令 “npm test”会调用此文件夹，在文件夹中需要引入待测试文件。 |
|  .vscode   |  Visual Studio Code 配置文件,里面包含着**仅适用于当前目录的**VS Code的设置 |
|   android  | 	Android的原生开发项目目录，包含了使用AndroidStudio开发项目的环境配置文件，可以用[Android Studio](https://www.baidu.com/s?wd=AndroidStudio&tn=24004469_oem_dg&rsv_dl=gh_pl_sl_csd)打开进行原生开发。| 
|   ios  | 	iOS原生开发项目目录，包含了XCode的环境，可以用[Xcode](https://www.baidu.com/s?wd=Xcode&tn=24004469_oem_dg&rsv_dl=gh_pl_sl_csd)打开进行原生开发  | 
|   node_modules  | 	基于node文件依赖系统产生的相关依赖和第三方lib， 存放所有的项目依赖库，配置package.json之后执行“npm install”后自动创建的文件夹。| 
| .babelrc	| Babel的配置文件,Babel是一个广泛使用的转码器，可以将ES6代码转为ES5代码，从而在现有环境执行。babelrc用来设置转码规则和插件。| 
| .buckconfig| 	buck的配置文件，buck是[Facebook](https://www.baidu.com/s?wd=Facebook&tn=24004469_oem_dg&rsv_dl=gh_pl_sl_csd)推出的一款高效率的App项目构建工具。| 
| .flowconfig	| Flow 是 Facebook 旗下一个为 JavaScript 进行静态类型检测的检测工具。它可以在 JavaScript 的项目中用来捕获常见的 [bugs](https://www.baidu.com/s?wd=bugs&tn=24004469_oem_dg&rsv_dl=gh_pl_sl_csd)，比如隐式类型转换，空引用等等。| 
| .gitattributes| 	git属性文件设定一些项目特殊的属性。比如要比较word文档的不同；对strings程序进行注册；合并冲突的时候不想合并某些文件等等。| 
| .gitignore| 	git配置文件，用于忽略你不想提交到Git上的文件| 
|  .watchmanconfig	| watchman的配置文件，watchman用于监控文件变化，辅助实现工程修改信息。| 
|   app.json  | 	配置了name和displayName，不过没发现在哪里使用到了。（待研究。。）  | 
| index.android.js	|  android的入口文件，可以在android的MainApplication中的ReactNativeHost中重写getJSMainModuleName()方法更改 | 
| index.ios.js	|  ios的入口文件，在Ios的AppDelegate.m文件的didFinishLaunchingWithOptions方法中通过jsBundleURLForBundleRoot可以更改入口文件| 
| package.json	| package.json定义了项目所需要的各种模块，以及项目的配置信息（比如名称、版本、许可证等元数据）。npm install命令根据这个配置文件，自动下载所需的模块，也就是配置项目所需的运行和开发环境  | 
| yarn.lock|   Yarn 是 一个由 Facebook 创建的新 JavaScript 包管理器；每次添加依赖或者更新包版本，yarn都会把相关版本信息写入yarn.lock文件。这样可以解决同一个项目在不同机器上环境不一致的问题。  | 

##3. 结构分析
