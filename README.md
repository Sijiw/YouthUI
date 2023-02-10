# 项目结构使用说明

该项目基于文章[使用vitepress从0搭建自己的组件库文档 - 掘金 (juejin.cn)](https://juejin.cn/post/7101117617233985566)构建，更多项目说明见该文章。

> 本项目包管理使用npm安装，启动时尽量使用npm，避免发生错误（使用yarn已出现一个BUG）。
> 

项目结构除了常规vue项目应有的目录和文件，新增packages和script目录。

其中，packages目录用于存放设计的编写好的组件，script是关于命令行生成组件目录的脚本文件。

## 如何创建一个新组件？

在终端中输入以下语句

```jsx
npm run gen
```

根据出现的提示输入信息即可，对应的组件存放在packages里。

## 组件目录中的内容

一个新建的组件内容如下图：

![Untitled](%E9%A1%B9%E7%9B%AE%E7%BB%93%E6%9E%84%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E%20187b8eabe4bc4fb080f178a5e552e161/Untitled.png)

其中，docs是文档目录，用于编写该组件的文档，由`README`引入`demo.vue`文件，通过`vite-plugin-md`插件解析markdown来展示文档。

src目录是编写组件的目录。

## 关于样式

样式文件在`src/style`中编写，已经配置好了颜色变量，从[Color 色彩 | Element Plus (element-plus.org)](http://element-plus.org/zh-CN/component/color.html)中查找，但是每种只配置了一个颜色，如果需要进行同类颜色修改还需要用Less的计算。

关于大小，需要根据自身设计组件而定，每种组件都不一样，所以暂不设定。
