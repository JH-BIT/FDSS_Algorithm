# 2020复旦大学软件/计算机保研机考：算法与数据结构总复习OxO

## Contributions

- 欢迎各位同学随意clone/fork，大家一起为了保研机考冲刺吧⁄(⁄ ⁄ ⁄ω⁄ ⁄ ⁄)⁄
- 如果有好的题目资源欢迎提issue哦_(:з」∠)_
- 同时欢迎前辈学长/学姐提供往年的考题/参考资料(/ω＼)
- 如果觉得不错就点个star叭（星星眼.jpg

## 经典考题(Python版答案详见exams文件夹下哦OvO)

### 第一部分（0.1-0.10）

- 连续最长子序列和
- 最短路径问题
- 逆波兰式判断表达式合法与求值
- 找出图中从节点s到t总权重小于等于k的情况
- 斐波那契型数字判别问题
- 数组逆序对计数
- 快速幂的板子题，输入a,b,c，输出pow(a,b)%c的值
- 组合数的经验题，输入一个n，输出组合数集合C(0,n) ,C(1,n) ,..., C(n,n)~ 中共有多少奇数。（第k个组合数与n异或后仍为k的个数）
- 奶牛吃草的问题（图的着色板子题（二分图），输出着色方案中字典序最小的那个）——鲍威尔算法/贪心算法
- 编辑距离

### 第二部分（1.1-1.10）

- 商店中有若干商品，它们也会打包在一起优惠出售，现给出需要购买的商品数量，求最低购买价格。要求购买的商品数量刚好符合题目要求。

eg：

输入信息：[2,4],[[3,0,5],[1,2,10]],[3,2]

题目解释：

输入：第一个矩阵是商品单买的价格，第二个矩阵为各种打包售卖时的数目与价格，第三个矩阵是各类商品需要购买数量

输出：最低价格

举例：商店中有A、B两种商品，A价格为2元，B价格为4元；优惠组合一包含3个A商品，0个B商品，共5元；优惠组合二包含1个A商品，2个B商品，共10元；现在要购买3个A商品，2个B商品；

答案：最低价格是，购买1个优惠组合一（含3个A、0个B），5元；再单独购买2个B，8元；共计13元

输出信息：13

- 一个有序三元组（a,b,c）, 1<=a<=X,

1<=b<=Y, 1<=c<=Z，且a，b，c皆为正整数。

给定X,Y,Z求所有能够形成三角形的(a,b,c)的数目。(3,4,5)和(3,5,4)为两个三角形。

输入:X Y Z（三个数都在1到10的九次方之间）

输出数量。输出结果对1000000007取模。

样例:

输入：2 3 3

输出：9

- 寻找“happy number”：

happy

number定义：一个正整数，其各位上的数字平方和加和得到新的数字，重复有限次的此操作，若最后得到结果1则是happy number，若形成某个循环则不是happy number。

输入若干正整数（每个数字均在10000以内），如果这个数字是happy number则输出这个数变成1经历的操作次数，否则输出循环体的第一个数。输入以0结束。

举例：输入17，经变换得到：50,25,29,85,89,145,42,20,4,16,37,58,89，则不是happy number，第一个循环的数是89，输出89；

输入28，经变换得到：68,100,1，是happy number，操作3次得到1，输出3。

- 数字一条龙输出：

第一行输入两个数：要格式输出的数字数目m和输出的宽度n，第二行输入m个正整数，将其按升序一条龙输出，要求换行处不得有多余空格。

举例：

输入1：

12 5

1 23 4 5 9 8 7 6 10 12 11

输出：

1 23 4 5

10 98 7 6

1112

输入2：

5 3

1016 95 42 3

输出：

3 1016

9542

- 给出一个二叉查找树的前序遍历（不超过40个节点），要求判断是否是平衡二叉树，输出yes或no。

这题应该是先还原出来这棵树，然后通过BFS记录叶子节点的深度进行比较之类。但由于我比较懒，就直接当成完全二叉树做了，直接比较每个节点左右孩子数在数量上是否会出现差了不只一层的情况，于是部分通过。

- “朋友圈”问题：

一共有m个学生（编号1到m，m大于3但不超过10000），其中某些学生之间是朋友关系，朋友关系不传递（这里看出不是并查集算法）。在其中n个学生组成的小社团中，学生A在这n个人中拥有的朋友数称为其在这n个人中的“欢迎度”。

输入：

第一行输入学生总数m和朋友关系n，随后n行输入拥有朋友关系的学生编号x1和x2；

然后输入社团数k，随后k行先输入社团人数p（3<=p<=m），再输入该社团的p个学生编号。

输出：

依次输出k行数，每行输出三个数字表示对应的社团欢迎度最高的前三个同学编号，欢迎度一样的按照字典升序输出。

思路：这道题应该是建一个大小为m的数组表示m个同学的朋友集合，每个数组后面接一个链表将其朋友连接起来，每次查询的时候访问对应的链表计数即可。但这题我也偷了懒（我怎么这么懒啊），直接用的STL里面的vector代替的链表，然后就TLE了。。。然后也懒得改了。。。（事实证明还是勤快些好呀T_T）

<!-- ## karekare算法日记

## 7.14

- 树相关问题复习
- 动态规划相关问题复习
- 排序算法复习

<!-- ## 7.18

- 哈哈。交大面试要完啦 -->

## 7.19

- minDifficulty：从递归到dp的优化

## 7.31 & 8.1 & 8.4 & 8.5

树/图的最短路径算法总复习 -->

## 项目结构说明

- basic 必须掌握的算法与数据结构知识点，不然不pay做cs学生哟

- book_exercise 随缘写一点CLRS练习题，预计会根据章节/页码编排哟

- exams 是README.md中经典考题的答案哟

- features Python的独特语法特性整理哟

- java 一些常见算法的java版本 更新频率会低于python版哟

- jzoffer 《剑指offer》的python版解答哟

- labuladong 记录每篇文章的核心题解和代码哟

- leetcode 随缘单刷些leetcode题 更新频率会低于其他目录哟

- nowcoder 每周日定时提交各大厂校招笔试题哟

- others 随缘搞些其他的题目来做做哟

- templates 把basic的代码进一步根据模板分类哟

- xiaozhao 虽说不准备本科直接工作，但也海投了一波嘻嘻（记录一些面试的手撕算法题 根据不同的公司分类哟）

- summary.md 预计会放一些常见算法思路/套路哟

## 爱我就点个star哟🌟 不然kare子可是会生气的哟（错乱

star star 我要star
比起这些 快给我star呀


