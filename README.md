### 项目介绍
提供基于wepy的zanui风格的组件, 简单易用, 开发方便.
### 使用方法
#### 1.安装wepy
本项目基于wepy开发
```
npm install -g wepy-cli
```
#### 2.体验代码
下载此仓库
```
git clone git@github.com:Zack-Bee/wepy-zanui-components.git
cd wepy-zanui-components
npm install
wepy build -w
```
在微信web开发者工具中选择此项目的根文件即可预览效果

#### 3.使用组件
将此项目中的components下你需要使用组件的文件夹移入你的components文件夹即可
```
代码调用
<template>
<Button :bindTap="bindTap">我是一个按钮</Button>
</template>

<script>
import wepy from "wepy"
import Button from "path/to/components/button/button"
export default class Index extends wepy.page {
    components = {
        Button
    }

    data = {
        bindTap: (event) => {
            console.log(event)
        }
    }
}
</script>
```
使用的设置与参数基本与[zanui小程序文档](https://www.youzanyun.com/zanui/weapp#/zanui)相同, 不同的地方在于参数基本上都是小驼峰式, 例如bindTap, 以及相关的事件处理都是通过将函数当作数据传入的, 我比较喜欢这样的方式. 最开始是打算使用这个库[wepy-zanui-demo](https://github.com/brucx/wepy-zanui-demo), 但是设计的方式和我喜欢的方式不同, 所以就自己造轮子. 源码写的比较清晰, 如果觉得没有文档的话可以直接看组件的源码.
