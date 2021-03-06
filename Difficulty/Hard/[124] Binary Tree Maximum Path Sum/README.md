# 问题描述

给定一个非空二叉树，返回其最大路径和。

本题中，路径被定义为一条从树中任意节点出发，达到任意节点的序列。该路径至少包含一个节点，且不一定经过根节点。

示例 1:

```bash
输入: [1,2,3]

       1
      / \
     2   3

输出: 6
```

```bash
输入: [-10,9,20,null,null,15,7]

   -10
   / \
  9  20
    /  \
   15   7

输出: 42
```

# 方法

这题容易想到使用递归的方法进行求解，不过需要考虑清楚，有三种情况：
考虑一个子树
```bash
    a
  /   \
 b     c
```
一种是bac的路径，第二种是ba然后a的根节点的路径，第三种是ca然后a的根节点的路径，其中递归函数返回的是后两种最大路径的和，第一种需要与全局最大sum进行比较。