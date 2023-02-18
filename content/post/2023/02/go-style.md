---
title: '自用的Go语言规范'
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

## 注释

Google: https://google.github.io/styleguide/go/decisions#comment-line-length

exported 的函数和方法其实都应该写, 不过从实践来看团队无法执行, 摆烂吧

## Package

### 包命名

Google: https://google.github.io/styleguide/go/decisions#package-names

包名会和变量名, 类型名一起出现在代码中, Go 不像其他语言使用`use ste::time::Duration`这种方式声明, 使用时直接使用`Duration`接口, 而 Go 只能通过`time.Duration`来声明, 也就是类型前面都会带上包名, 我在实践过程中遇到很多次这个包名会很长, 不管是 Google 推荐的那种直接小写字母连写`tabwriter`,还是下划线分割`tab_writer`都有点丑, 我个人喜欢下划线, 可读性更好一点吧
