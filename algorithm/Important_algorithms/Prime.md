## Prime
### 目标
求最小生成树。
### 内容
设顶点集合`S`，联通分量`M`
1. 取任意顶点加入`M`。
2. 于每一次迭代从`S`将 `dist(M,Si), Si <- S`最小的节点加入`M`,直到`S`为空集。
### 效率
![[Pasted image 20220617134833.png]]
### 特性
1. 属于贪心算法