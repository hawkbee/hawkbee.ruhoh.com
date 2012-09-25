---
title: diff与patch
date: '2012-09-25'
description:
categories: shell
tags: diff
---

如果代码有变动，怎么快速找出这些变动，如何在其它的代码树中快速应用这些修改，如何与他人快速共享你的修改。diff与patch工具就是实现这些的必杀技。这两个工具是共享修改的基本技能，如果需要频繁共享更新代码，建议采用`svn`，`git`等进阶工具。

基本使用方式`diff -Nru base modify > patch.diff`，`patch -p1 < patch.diff`，更强大的功能`man diff`，`man patch`。

### diff的格式

 * normal diff - 只记录了变更行。
 * context diff - 将变更行的上下文记录下来。
 * unified diff - 在context diff的基础上对记录的上下文进行了合并。

这三种格式生成方式为，diff程序默认生成normal diff格式，`-c`生成context diff格式，`-u`生成unified diff格式。


