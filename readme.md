# VSC中使用scss
## 插件扩展中搜索：Live Sass Compiler
## 在vsc用户设置中搜索： Live Sass Compiler找到settings.json编辑中找到liveSassCompile.settings.formats的配置项，将"savePath"的值改成："~/../css/"
## 在目录下创建scss和css文件夹，并在scss文件夹里创建style.scss文件
## 在vsc的命令面板中输入（ctrl+shift+p）：>Live Sass:Watch Sass开启，此时css文件夹中自动增加.css文件
### 在插件扩展中搜索：css-auto-prefix，安装兼容浏览器css输入插件

### 引入外部scss文件（@import）
* 外部scss文件名：_public.scss
* 主scss文件中：@import "public" 引入外部scss文件
### 设置变量
* 定义变量：$fs12: 12px;
* 变量使用：font-size: $fs12;
### 继承
* 父类：%borderB{
    border-width:0 0 1px 0;
    border-color:#eee;
    border-style:solid;
}
* 子类：span{
    color:#fff;
    @extend %borderB
}
### 函数
* 定义方法：@mixin transform($type){
    transform: $type;
    -webkit-transform: $type;
    -moz-transform: $type;
    -ms-transform: $type;
    -o-transform: $type;
}
* 使用函数：@include transform(rotate(-10deg))