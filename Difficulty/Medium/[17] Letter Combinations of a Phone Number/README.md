# 描述 
给定一个包含2-9个数字的字符串，返回该数字可能表示的所有字母组合。下面给出了数字到字母的映射(就像电话按钮一样)。注意，1不映射到任何字母。

![](Telephone-keypad2.png)
# 例子

```bash
Input: "23"
Output: ["ad", "ae", "af", "bd", "be", "bf", "cd", "ce", "cf"].
```

# 方法
方法很简单，根据数字判断当前的起始英文字符以及该数字下有多少个英文字符，初始化结果为第一个数字代表的字符，然后依次循环其他数字，得到他们的字符，与res进行双层循环，使用temp对新字符串进行存储，然后赋值到res中，整个过程一遍成功，并且c++速度超越100%的提交，Nice！