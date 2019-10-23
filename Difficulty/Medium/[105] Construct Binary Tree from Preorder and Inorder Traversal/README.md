# 问题描述

根据一棵树的前序遍历与中序遍历构造二叉树。

注意:
你可以假设树中没有重复的元素。

例如，给出
```bash
前序遍历 preorder = [3,9,20,15,7]
中序遍历 inorder = [9,3,15,20,7]
```

返回如下的二叉树：
```bash
    3
   / \
  9  20
    /  \
   15   7
```

# 方法

先序遍历的第一个节点就是根节点，根据根节点可以在中序遍历的数组中找到根节点的位置，由于是中序遍历，那么根节点所在的位置的左边就是左子树，右边即为右子树，就可以知道左子树和右子树的节点个数，然后根据先序遍历会先访问完根节点左子树的节点，然后在访问右子树的节点，根据左子树节点个数，可以定位左子树先序遍历数组的末尾位置，末尾位置的下一位即为根节点的右子树，而根节点的左子树为先序遍历的第二个元素。这样就分解成了两个子问题，经过同样的方式去寻找相应的父节点。

更通俗的图解在https://leetcode-cn.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/solution/cong-qian-xu-he-zhong-xu-bian-li-xu-lie-gou-zao-er/