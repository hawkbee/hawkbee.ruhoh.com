---
title: git rebase的使用
date: '2012-09-18'
description:
categories:
---

在标准的git协作流程中，通常要求在完成本地修改后，在开发者在请求集成者合并到主干前，需要进行一个rebase的操作，那么这个rebase操作的目的是什么呢，到底要达到一个什么目的，这个过程又完成了那些操作呢？带着这些疑问，让我们走进rebase。

### rebase的使用方法

	$ git rebase [--onto <newbase>] [<upstream>] [<branch>]
		将<branch>分支相对于<upstream>分支的修改，重新应用到<newbase>分支上。

	$ git rebase <upstream> <branch>
		<newbase>默认为<upstream>。

	$ git rebase <upstream>
		<newbase>默认为<upstream>，<branch>默认为当前分支。

### 为什么要使用rebase
通过rebase，你可以将在一个分支上的所有修改重新应用到另外一个分支上（重放提交）。

### rebase工作过程
通过找到两个分支的共同提交（`upstream`与`branch`），找到`branch`分支中每一个提交，保存这些提交到临时文件中，然后将每一个提交应用到`newbase`分支上。

### 应用场景

