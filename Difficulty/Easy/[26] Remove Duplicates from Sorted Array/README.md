# 问题描述
给定一个已排序的数组号，删除重复项，使每个元素只出现一次，并返回新的长度。O(1)额外内存.

# 例子
```bash
nums = [0,0,1,1,1,2,2,3,3,4],

返回length = 5, 第一个到第五个元素依次修改为0, 1, 2, 3, and 4.
```

# 方法
对前后相同重复的元素进行计数，遇到前后不相同的元素，使用计数值定位前面重复的值，使用当前值替换。