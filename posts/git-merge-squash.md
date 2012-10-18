---
title: squash选项在git合并时的使用
date: '2012-10-16'
description:
categories: scm
tags: git
---

> Produce the working tree and index state as if a real merge happened (except for the merge information), but do not actually make a commit or move the HEAD, nor record $GIT_DIR/MERGE_HEAD to cause the next git commit command to create a merge commit. This allows you to create a single commit on top of the current branch whose effect is the same as merging another branch (or more in case of an octopus).
>
> With --no-squash perform the merge and commit the result. This option can be used to override --squash.

工作目录与index状态与真正的合并完全一致（除合并信息之外），不完成提交与移动HEAD，也不在$GIT_DIR/MERGE_HEAD中记录以生成合并提交。允许在当前分支生成一个单一的提交，而效果与合并另外一个分支一致。
如果在一个分支上提交了大量的临时记录，可以通过该选项为该分支形成一个干净的提交记录。

=== 推荐工作流程

1. 基于主分支创建一个私有分支。
2. 在私有分支上进行开发工作。
3. 代码完善后就清理掉私有分支的历史。
4. 将干净的私有分支合并到主分支中。
