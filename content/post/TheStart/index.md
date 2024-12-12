+++
weight = -1
image = 'hugo-logo-wide.svg'
categories = ['瞎折腾']
date = '2024-12-11T21:28:16+08:00'
title = '一切的开始'
description = '用 Hugo 搭建的个人博客'
tags = ['Hugo', '博客']
lastmod = '2024-12-11T21:31:00+08:00'
+++

## 关于

本博客由 [Hugo](https://gohugo.io/) 搭建，由于框架非常简单，事实上我并没有做什么实质性的工作，多半就是在已有的模板上修修改改而已。

## 主题

大部分主题样式照搬了 [Hugo Theme Stack](https://github.com/CaiJimmy/hugo-theme-stack)，自己做了一些修改，希望以后可以自己完善或添加一些功能。

## 寄语

希望能在这里分享一些我在学习过程中遇到问题然后解决的方法，希望能坚持下去（真的可以吗。。。。

## 测试

以下为测试内容

### 列表测试

- 无序列表项 1
  - 嵌套无序列表项 1.1
  - 嵌套无序列表项 1.2
- 无序列表项 2

1. 有序列表项 1
2. 有序列表项 2
   1. 嵌套有序列表项 2.1
   2. 嵌套有序列表项 2.2

### 引用测试

> 这是一个引用块。

### 带有归属的引用

> Don't communicate by sharing memory, share memory by communicating.<br>
> <cite> --- Rob Pike[^1] </cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

### 代码测试

```python
# 中文测试
def hello_world():
    print("Hello, World!")
```

### 链接测试

[Hugo 官网](https://gohugo.io/)

### 图片测试

![Hugo Logo](hugo-logo-wide.svg)

### 表格测试

| 表头 1 | 表头 2 | 表头 3 |
| ------ | ------ | ------ |
| 内容 1 | 内容 2 | 内容 3 |
| 内容 4 | 内容 5 | 内容 6 |

### 粗体和斜体测试

**这是粗体文本**

_这是斜体文本_

**_这是粗体加斜体文本_**

### 分隔线测试

---

### 任务列表测试

- [x] 已完成任务
- [ ] 未完成任务

### Shortcodes 测试

#### Bilibili 视频

{{< bilibili BV1pzq3YiEqe >}}

#### 带源的引用

{{< quote author="A famous person" source="The book he wrote" url="https://en.wikipedia.org/wiki/Book">}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
{{< /quote >}}

#### PDF 查看

{{< pdf "最优化方法大作业.pdf" >}}