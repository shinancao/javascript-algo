## 回溯算法的框架

```
result = []
def backtrack(路径，选择列表)：
  if 满足结束条件：
    result.add(路径)
    return
  
  for 选择 in 选择列表：
    做选择
    backtrack(路径，选择列表)
    撤销选择
```

选择列表也有可能是每一阶段要去决策的位置。如果得到的组合中是允许重复元素出现的，那参数就是位置，比如`pos`，在`for`循环中到下一阶段传的是`pos + 1`，而不是`i + 1`。如果不允许重复的出现就用`i + 1`，就将之前选过的值排除掉了。

## 多叉树的递归遍历

```
void traverse(TreeNode root) {
  for (TreeNode child: root.children) {
    // 前序遍历需要做的操作
    traverse(child)
    // 后序遍历需要做的操作
  }
}
```

来源：<https://labuladong.gitbook.io/algo/suan-fa-si-wei-xi-lie/hui-su-suan-fa-xiang-jie-xiu-ding-ban>