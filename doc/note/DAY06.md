# 30. 关于VUE Cli

VUE Cli：Vue脚手架

在Vue脚手架项目中，使用的是“单页面”的设计模式，也就是说，整个项目中只有1个HTML，而这个HTML是由多个不同的视图组合而成的，每个视图都是可以随时替换为其它视图的，并且，每个视图都由独立的文件来开发。

关于Node.js的安装、VUE Cli的安装，请参考《VUE Cli课前准备_软件安装篇》教程。

# 31. 修改VUE Cli项目的端口号

打开项目下的`package.json`，原本有以下代码片段：

```json
"scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build"
},
```

将以上`serve`属性的值后面添加`--port 指定的端口号`即可修改端口号，例如：

```json
"scripts": {
    "serve": "vue-cli-service serve --port 9000",
    "build": "vue-cli-service build"
},
```

修改完后，重新启动项目，即可看到占用了`9000`端口。

# 32. VUE脚手架项目的结构

Vue脚手架项目的结构：

- `[.idea]`：只要是使用IntelliJ IDEA打开的项目，都会生成此文件夹，是IntelliJ IDEA管理项目时使用到的相关文件，此文件夹不应该手动修改，如果此文件夹中出现错误，将此文件夹删除即可，后续IntelliJ IDEA会自动重新创建此文件夹及内部的文件
- `[node_modules]`：当前项目中的依赖项文件所在的文件夹（Vue脚手架项目的依赖项都在当前项目中，不像Java项目的依赖项统一在`.m2\repository`下），此文件夹不应该手动修改，在使用GIT管理项目时，此文件夹通常会被配置到`.gitignore`文件夹，以至于此文件夹不会被提交到GIT服务器，当从其它电脑上拉取项目时，也不会得到此文件夹及内部的文件，则项目是不可以运行的，需要在项目文件夹下执行`npm install`命令，会自动创建此文件夹，并根据`package.json`中配置的依赖项来下载所需的所有依赖项
- `.gitignore`：所有使用GIT管理项目都有此文件，用于配置GIT应该“忽略”的文件或文件夹
- `package.json`：当前项目的配置文件，在创建项目时需要指定此文件作为配置文件，此文件中主要配置了npm命令的相关脚本、当前项目的依赖项
- `package-lock.json`：是锁定的配置文件，是根据`package.json`自动生成的，不可手动修改







