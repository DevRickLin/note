![[Pasted image 20220617103354.png]]

## Multistage graph problem
![[Pasted image 20220616100806.png]]
从`t`往`s`向后通过递推关系式求解：
![[Pasted image 20220616100750.png]]
## Longest path in DAG
![[Pasted image 20220616100917.png]]
![[Pasted image 20220616100912.png]]
## Edit Distance 
编辑距离的直观解释便是，从一个字符串 `s1` 到 `s2`需要做多少步操作。
操作可以分为
1. 删除不同的字符
2. 将不同的字符插入目标字符串
3. 将不同的字符取代目标字符串

以上三个操作的步数同为`1`。
设`ed(s1,s2,m,n)`代表`s1[0..m]`及`s2[0..n]`字符串的编辑距离，则编辑距离的动态规划算法可以表示如下
```javascript
function min(a,b,c){
// return min value;
}
function ed(s1,s2,m,n){
	if(s1[m] === s2[n]){
		return ed(s1,s2,m-1,n-1);
	}
	return min(
		ed(s1,s2,m-1,n), // 删除s1[m] 后， 只需取 s1[0..m-1] 和 s2[0..n] 的编辑距离 + 1
		ed(s1,s2,m,n-1), // 插入s2[n] 到 s1末尾
		ed(s1,s2,m-1,n-1) // 直接将s1[m]替换为s2[n]
	) + 1
}
```
## Knapsack
![[Pasted image 20220616102421.png]]

直观描述01背包的动态规划思想，是当前 取到第 j 个 物品， 总容量为 w 的背包，可以由两个背包演化而来：
1. 取到 j -1 个物品，已经在容量w下放满的背包。
2. 取到 j-1 个物品，有留下当前物品空位（`w-w(j)`）的背包。
有时候放满的背包价值比较高，有时候则是再放入当前物品后价值更高。

需要注意初始化的过程，也要符合递归式的规律。代码则需要处理对负容量背包的访问。若是存在负权值的物品，不可初始化为`0`而应当是负无穷。
## Chain matrix multiplication
(待补充)
## All pairs shortest path
如果在加入某个节点后，可以使得路径变短，则加入该节点，否则维持原样，节点的枚举从 1 ... k 为止。 
![[Pasted image 20220616103433.png]]
## Traveling Salesman
![[Pasted image 20220616105021.png]]

