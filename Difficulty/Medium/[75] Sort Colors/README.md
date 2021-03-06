# 问题描述

给定一个包含红色、白色和蓝色，一共 n 个元素的数组，原地对它们进行排序，使得相同颜色的元素相邻，并按照红色、白色、蓝色顺序排列。

此题中，我们使用整数 0、 1 和 2 分别表示红色、白色和蓝色。

**注意:**
不能使用代码库中的排序函数来解决这道题。

# 例子

```bash
输入: [2,0,2,1,1,0]
输出: [0,0,1,1,2,2]
```

**进阶：**

一个直观的解决方案是使用计数排序的两趟扫描算法。
首先，迭代计算出0、1 和 2 元素的个数，然后按照0、1、2的排序，重写当前数组。
你能想出一个仅使用常数空间的一趟扫描算法吗？

# 方法

方法采用的是双指针(更准确的说是三指针），建议查看这个[discuss](https://leetcode.com/problems/sort-colors/discuss/26474/Sharing-C%2B%2B-solution-with-Good-Explanation), 由于数据只有3种大小，这个方法中设立了三个变量，left, middle和right，left表示0的右边界，right表示2的左边界，通过mid的值进行判断是否与left或者right进行交换。

