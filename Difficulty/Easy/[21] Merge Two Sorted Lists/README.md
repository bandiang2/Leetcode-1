# 问题描述
合并两个已排序的链表，并将其作为一个新列表返回。新列表应该通过将前两个列表的节点拼接在一起来创建。

# 例子
```bash
Input: 1->2->4, 1->3->4
Output: 1->1->2->3->4->4
```

# 方法
方法一：使用递归方法来做，上面的第一个链表是[1, 2, 4], 第二个是[1, 3, 4], 一次比较后又是两个新的链表（[2, 4]和[1, 3, 4]）进行合并，所以这是一种递归形式。

方法二：使用迭代方法来做，循环条件是两个链表非空，在循环内部进行比较和赋值结点。