---
title: 莫图形化编程炫舞软件的脱壳实践
published: 2025-03-01
description: ""
image: ""
tags: []
category: ""
draft: false
lang: ""
---

莫图形化编程炫舞软件脱壳实践

## 前言

被拜托破一下新的小鸟飞飞（2.2.0）

但在使用 reflector 进行分析时发现部分代码被加密（hh 绝对是之前太狂了直接在吾爱上写小鸟飞飞然后 seo 第一个就是我的文章！，还是得想个办法改改不然也挺难办的）

不过该弄还是得弄，于是便有了这篇文章

## 过程

首先直接使用 Exeinfo PE 查壳（https://github.com/ExeinfoASL/ASL）

安装后将主 exe 拖入 Exeinfo PE 后查到.NET ConfuserEx，搜了一下找到是一个开源的壳https://github.com/Desolath/ConfuserEx2 然后看到有一份 Unpacker https://www.52pojie.cn/thread-1304627-1-1.html之后再下一下在help里面提到的de4dot https://github.com/kant2002/de4dot 结束

---

把主文件拖到 ConfuserEx-Unpacker.exe 文件，然后将生成的-cleaned 文件拖给 de4dot.exe，最后将生成的-cleaned-cleaned 文件重命名回 `小鸟飞飞图形化编程炫舞软件.exe`然后替换在安装目录的原 exe

---

然后继续使用 reflector 修改程序即可（参阅我原先的文章

莫图形化编程炫舞软件破解实践
https://www.52pojie.cn/thread-1915961-1-1.html
(出处: 吾爱破解论坛)

）
