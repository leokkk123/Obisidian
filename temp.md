1. 构思->实现->测试
2. 左到右，差错效率递减

数据结构来判断 **是否有重复的字符**，常用的数据结构为哈希集合（即 `C++` 中的 `std::unordered_set`，

1. 怎么比较是同构还是异构？
		最简单办法就是用umap/uset来进行比较。要么就两个循环
 2. 前缀和还能解决什么样的问题？
	 1. 前缀和是什么？前缀和是计算从0-i的和，放到一个hash_map中去，第二个值可以有不同的作用
3. 正常的优化思路事从暴力便利到优化其中一部分的数据结构
4. 动态规划：
	1. 主要解决什么问题？
	2. 无后效性：动态规划问题设计状态的技巧
	3. 怎么推导状态方程
	4. 最后优化空间
	5. key：字问题定义
;
 6. dp[i][j]:
	 1. dp[i]:是一个vector
	 2. dp[i][j]是一个int
O(n)
1. 滑动窗口，两个指针各只走一遍:连续子数组
2. 前缀数组和：便利一遍的同时，将前缀数组存放到hash表中，实际上可以做更多事，比如将前缀数组换成更复杂的数据。或者将int转换成pair等更加复杂的数据

怎么判断一个数是整数
```
double num = 42.0;

if (num == static_cast<int>(num)) {
    std::cout << "The number is an integer." << std::endl;
} else {
    std::cout << "The number is not an integer." << std::endl;
}

```

1. std::string::npos
2. string::erase会删除自身的
3. dp[""]=true;是允许的
```cpp
for(int i=s.length()-1;i>=0;i--)是可以的
如果写作 size_t i则是不行的，因为size_t 是无符号数，<0后会变为巨大的整数。。
```