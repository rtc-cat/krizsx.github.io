---
title: "自用的Go语言规范"
date: 2023-02-18T15:52:24+08:00
draft: true
comment: true
---

个人不太喜欢 Google 官方的一些规范

<!--more-->

# 背景

写 Go 的过程总感觉很折磨, 包括命名, 错误处理, 日志, 类型系统等等, 一直都选择了摆烂, 能跑就行的原则,
现在感觉是时候需要给自己指定一些规范和代码模板, 不然总觉得开发效率很低

大量内容参考: [Google Golang style guide](https://google.github.io/styleguide/go/)

# 规范内容

按照一个文件中的编码顺序排列规范内容

## 命名

1. 包名用小写下划线分割, snake_case
2. 接口有 I 开头, `IWorker`
3. 方法接收者用`self`
