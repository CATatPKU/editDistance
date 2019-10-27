# editDistance
# PPT

---

## 词相似度计算（佳音）
### Damerau–Levenshtein distance（D氏距离）
#### 定义
- D氏距离是用来测量两个字符序列之间的编辑距离的字符串度量标准。                      
#### 计算原理
- Optimal string alignment/restricted Damerau-Levenshtein distance（严格编辑距离）：
	
- Adjacent transpositions（交换相邻项算法）

---

### Longest Common Substring & Longest Common Subsequence （最长公共子序列与最长公共子串）
#### 定义
- 最长公共子串问题是寻找两个或多个已知字符串最长的子串。
#### 计算原理
- 当序列的数量确定时，问题可以使用动态规划在多项式时间内解决。

---

## 汉明距离
### 定义
两个等长字符串之间的汉明距离（Hamming distance）是两个字符串对应二进制位不同的位置的数目。

### 计算原理
对于二进制字符串a与b来说，它等于a 异或b以后所得二进制字符串中“1”的个数。

### 最小汉明距离

---

## Jaro距离
### 定义
The Jaro–Winkler distance (Winkler, 1990)是计算2个字符串之间相似度的一种算法。它是Jaro distance算法的变种。主要用于record linkage/数据连接（duplicate detection/重复记录）方面的领域，Jaro–Winkler distance最后得分越高说明相似度越大。Jaro–Winkler distance 是适合于名字这样较短的字符之间计算相似度。0分表示没有任何相似度，1分则代表完全匹配。

---



## 编辑距离

## BK树
### 介绍
BK树（Burkhard Keller Tree）的概念最早由W.A.Burkhard和R.M. Keller于1972年提出。这种树结构可以根据Levenshtein编辑距离概念进行拼写检查、字符串模糊匹配。许多软件中的自动校正功能都可以基于BK树结构完成。[^1].

---


**建树：**
bk树的建立基于Levenshtein编辑距离概念，定义d(x,y)为key x到key y的编辑距离。此外若有另一key z，则有如下性质成立：
- d(x,y)=0 #编辑距离为0，意为x=y
- d(x,y)=d(y,x)  #从x变到y的最少步数就是从y变到x的最少步数
- d(x,z)<=d(x,y)+d(y,z) #从x变到z所需的步数不会超过x先变成y再变成z的步数
其中第三点性质最为重要，由于和数学中的三角形不式（两边之和大于第三边）相似，被称作编辑距离中的三角不等式。

---

### 应用
#### 模糊匹配与错误纠正
##### 模糊匹配
在查找最相近字符串的基础上，很快有人提出如何利用BK树进行模糊匹配的问题。[^3]



---

## 句相似度计算（可欣）
### 相似度检测方法


#### 1. BOW

#### 2. TF-IDF

#### 3. Word2Vec 

   
#### 4.  词移距离

 
#### 5. Smooth Inverse Frequency

#### 6. 预训练编码器

---

#### 7. 基于LSTM的语句相似度计算方法
Siamese Network 是指⽹络中包含两个或以上完全相同的⼦⽹络，多应 ⽤于语句相似度计算、⼈脸匹配、签名鉴别等任务上：
 
---
 
## 树结构 （Humi）
### 语言学中的句法学

#### 乔姆斯基的转换生成语法

---

#### 转换生成语法中的句子结构

---

#### 涉及到语序问题



---


#### 句子相似度整体计算

结合上面两个方面，句子相似度既要考虑到语义层面还要考虑到句子语序问题。

![](images/Humi_6.png)

T1:  My little boy loves baking cakes. 

T2:  All girls like to bake cakes. 

T3:  Girls like going to cake-bakes. 

T4:  Some boys enjoy baking cakes. 

T5:  When I was a boy I occasionally baked cakes. 

T6:  This little baked cake is inedible.

T7:  Skidding cars bake my cakes every time. 

T8:  On the little hill it was baking hot and the boy was caked in mud.

![](images/Humi_7.png)






## 树结构和翻译记忆的关系

