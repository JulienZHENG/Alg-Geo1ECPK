# Définitions de “dimension finie”有限元章节的定义集合

## 2.1Base finie

### Combinaison linéaire 线性组合

线性组合：E中取向量组（$x_i $），在$K^I$中取一组数（$a_i $），则$x=\sum a_ix_i$形成的向量称为向量组（xi）的一个线性组合

> 本质上就是基于加法和数乘这两种**线性**运算所形成的组合，可以“顾名思义”来理解这个概念

若$a_i$不等于$b_i$，线性组合不一定不等

我们使用$Vect((x_i)_{i\in I})$来表示一个向量组famille的线性组合

![image-20221011191651798](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221011191651798.png)

### 向量子空间

$x$称为线性组合的值，或$x$可以被向量组（$x_i $）线性表出。所有$x$组成的集合称作由向量组($x_i$)张成的E的向量子空间。

![image-20221011191955097](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221011191955097.png)

### 向量组famille的性质：Génératrice, libre/liée, linéairement indépendants et linéairement dépendants    

定义原文：

2.1.1 Soit $(x_i)_{i\in I}$ une famille finie de vecteurs dans E. On dit qu’elle **génératrice** si tout vecteur de E est la valeur d’ au moins une combinaison linéaire des $x_i$ . On dit qu’elle est **libre** si tout vecteur de E est la valeur d’ au plus une combinaison linéaire des xi . On dit que cette famille est une **base** (finie) de E si elle est à la fois génératrice et libre.

![image-20221010173702512](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010173702512.png)

Génératrice：向量组合中的线性组合能够张成（span）到整个空间（空间内随便找个向量到可以找到其合适的线性组合）

> “张成”（英文span）是一个非常微妙而且形象的动词，为了更好地理解“向量空间”，张成的空间以及线性组合，推荐访问[【官方双语/合集】线性代数的本质 - 系列合集_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1ys411472E/?spm_id_from=333.999.0.0&vd_source=7adbdf47947e0c7c70d366d4115a8f20) 

linéairement indépendants et linéairement dépendants：线性相关与线性无关（这个很好理解，dépendants这个词用的很是精妙啊~~）

libre：指所有向量满足indépendant的（为什么用libre这个词？？？）——这时候会发现，对于这个向量组而言，空间里的向量对应的线性组合unique了

liée：libre的对立面

base(finie): 基底，对于向量族满足libre+génératrice$\rightarrow$base

> base canonique: 规矩的基底~~对于一个空间可以有不同种的基底，其中最“规矩”的就是 base canonique
>
> ![image-20221010205629292](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010205629292.png)

于是就有了On dit que l’espace vectoriel E est **de dimension finie** s’il existe une base finie de E.

### 与线性映射（application linéaire)的联系P16

2.1.4（重要重要！对后续的推导有很大的作用！）![image-20221010180553915](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010180553915.png)

> 复习：满射surjective 单射injective
>
> <img src="https://bkimg.cdn.bcebos.com/pic/7af40ad162d9f2d3c4f49999a2ec8a136227ccdb?x-bce-process=image/resize,m_lfit,w_440,limit_1" alt="img" style="zoom:67%;" />
>
> isomorphisme：同构映射（简称同构），对于两个群，之间存在一个**双射bijective**的映射，那么称这两个群是同构的，这一双射映射就被称为**同构isomorphisme**

证明充分利用了f作为application linéaire 的性质，详见教材

注意此题是在向量组上套一个**线性映射**（比如$x_i$到$2x_i$）故只改变向量的大小，不改变其线性相关性（除非变成0向量）

第一条满射意味着在映射后，向量组中的一部分向量因为其线性相关性而与其他向量重合消失，但剩下的向量组依旧可以长到整个空间。

### Système de coordonnées ou base duale 对偶空间

E*简言之就是提取出线性组合的数字（或者叫坐标coordonnée）

参考《高等代数》

以下摘自wiki monde 链接：[Base duale - Encyclopédie Wikimonde](https://wikimonde.com/article/Base_duale)

Soit *E* un [espace vectoriel de dimension finie](https://wikimonde.com/article/Espace_vectoriel_de_dimension_finie) *n* sur un corps *K*. Soit *B* = (*e*1, … , *en*) une [base](https://wikimonde.com/article/Base_(algèbre_linéaire)) de *E*, c'est-à-dire que tout vecteur *v* de *E* s'écrit de manière unique comme une [combinaison linéaire](https://wikimonde.com/article/Combinaison_linéaire) des vecteurs *ei* :

![v=\sum _{{i=1}}^{n}e_{i}^{*}(v)e_{i}\,,](https://wikimedia.org/api/rest_v1/media/math/render/svg/5ab610359268665d863a8cf32d0cd838d18f897b)

où ![e_{i}^{*}(v)](https://wikimedia.org/api/rest_v1/media/math/render/svg/d901d54dd1be252b457e1c532db134c618e1c7f7) est un [scalaire](https://wikimonde.com/article/Scalaire_(mathématiques)) (un élément du corps *K*). L'application ![v\mapsto e_{i}^{*}(v)](https://wikimedia.org/api/rest_v1/media/math/render/svg/2aa5a962f5aba9a8a0cc68fec557e587a7a06233) est une [forme linéaire](https://wikimonde.com/article/Forme_linéaire) sur *E*. L'application ![e_{i}^{*}](https://wikimedia.org/api/rest_v1/media/math/render/svg/4aac0dbbe3f6cbf9dfc247b64695cbea4d67e6b0) peut aussi être définie comme l'unique forme linéaire sur *E* vérifiant, pour tout entier *j* entre 1 et *n*, ![e_{i}^{*}(e_{j})=\delta _{{ij}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/26db85b344f48f20f1111b6ff1d088825f7baa51) où ![\delta_{ij}](https://wikimedia.org/api/rest_v1/media/math/render/svg/fa75d04c11480d976e1396951e02cbb3c4f71568) est le [symbole de Kronecker](https://wikimonde.com/article/Symbole_de_Kronecker) (qui vaut 1 ou 0 suivant que *i* et *j* sont égaux ou non).

> La famille (*e*1*, … , *en**) forme une base de l'espace dual *E**[1](https://wikimonde.com/article/Base_duale#cite_note-1), appelée la base duale de *B* et notée *B**.

---

---

## 2.2 dimension

### 2.2.1-2.2.6一些显然的结论，似乎记住用就好了~~

![image-20221010203835708](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010203835708.png)

![image-20221010203848274](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010203848274.png)

![image-20221010203903244](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010203903244.png)

![image-20221010204011933](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010204011933.png)

![image-20221010204051051](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010204051051.png)

### 2.2.7dimension的定义引出，即base中向量的数量![image-20221010204119308](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010204119308.png)

（注：dimension与后面2.3提到的的秩rang紧密相关，但是两个概念描述的是不同的东西）

显然：![image-20221010204311618](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010204311618.png)

### 2.2.9-2.2.10与映射的联系（通过映射来寻找向量空间的dimension）

### ![image-20221010204643334](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010204643334.png)

2.2.9翻译：对于一个**自同构**（endomorphisme）的向量空间，其中的映射要么是双射，要么非单非满。参考[2.1.4](2.1.4)证明非常容易

![image-20221010205403438](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010205403438.png)

![image-20221010205456481](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010205456481.png)

![image-20221010210401085](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010210401085.png)

？？？？？

---

---

## 2.3 Théorème du rang

*秩 （法：rang 英：rank）是一个神奇的概念，从向量组到映射再到矩阵，我们都使用了秩这一概念以描述他们的性质*

### 2.3.1子空间的dimension更低（显然）

![image-20221010210618406](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010210618406.png)



### 2.3.2 Codimentions余维数的定义

![image-20221010210753073](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010210753073.png)

（啊啊啊这个词是怎么来的呀？词缀co指的是？？？？？）

### 2.3.3 向量组的秩的定义

![image-20221010211306328](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010211306328.png)

### 2.3.4 线性映射的秩 定义：用映射的象Image的秩来描述

![image-20221010211359743](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010211359743.png)

### 2.3.5 （théorème du rang）

![image-20221010211807131](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010211807131.png)

![image-20221010212437723](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010212437723.png)

> 如何理解théorème du rang？
>
> 用线性代数的例子：Ax=b中（定理中的f被视为矩阵A，Im f对应列空间columnspace，Ker f对应着零空间nullspace，零空间与列空间的dimension之间的关系 .....（参考教材 Introduction to Linear Algebra by Gilbert Strang

### 2.3.6(有疑惑？？)

![image-20221010213801218](C:\Users\zxy64\AppData\Roaming\Typora\typora-user-images\image-20221010213801218.png)

