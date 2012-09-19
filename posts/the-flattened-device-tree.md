---
title: 扁平设备树
date: '2012-09-19'
description:
categories: Linux
---

>All the cool architectures are using device tree. I want to use device tree too!

在PowerPC的目录结构中，存在着一些以`.dts`结尾的文件，这些文件是用来干什么的呢？

"Open Firmware Device Tree"，或者简称为"Device Tree"，是一种描述硬件信息的数据结构和语言。更明确一点，它是一种硬件描述信息，可以被操作系统读取，从而操作系统不需要硬编码这些硬件信息。

从结构上来看，DT是一棵树，带有命名节点的无环图，每一个命名节点拥有任意数量的命名属性，命名属性带有任意的数据。同时也提供了建立链接到树外部节点的机制。

引用文献：

1. http://omappedia.org/wiki/Device_Tree
2. http://devicetree.org/Device_Tree_Usage
