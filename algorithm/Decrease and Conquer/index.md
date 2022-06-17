![[Pasted image 20220615173802.png]]
![[Pasted image 20220615195317.png]]
### Find Kth smallest element
找到第k个最小元素的办法，直觉便是排序再找，但如此一来时间复杂度就为排序算法所限制。而`quick_select`可以实现线性时间算法。
#### quick select
其大约可以分成三步。设要取的目标是`k`，函数签名为`fn select(arr,idx = 0)`
1. 取得适当的 pivot `x` 将目标数组`s`分为小于`x`的`s1`及大于`x`的`s2`，将`x`插入其中。
2. `x`下标`i`等于`k-1`的话，返回`x`，否则若`k-1 < i` 递归`select(s1,k)`，否则递归`select(s2,k-|s1+x|)`。

其思想便是减治，每次只需要搜寻其中的一半，时间复杂度`O(n)`
### Insertion Sort
一般的插入排序很好理解，不过可以通过递归的方式更加体现其减治特性。（插入完的部分都是有序的，去掉再递归）
### DFS
简单来说，就是不断朝任意一个未访问的邻接节点访问，直到该节点不存在未访问的邻接节点就回退，要是一路退退退回了初始节点，则结束。
### BFS
![[Pasted image 20220617093845.png]]

![[Pasted image 20220617093731.png]]
### Topological Sort
![[Pasted image 20220617094222.png]]
![[Pasted image 20220617094246.png]]