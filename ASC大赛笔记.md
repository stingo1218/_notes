# 1.信息检索

涉及:

**自然语言处理**-文本处理(计算语言学)

**数据挖掘**-信息分类聚类预测

**机器学习**

**大数据处理**-

## 1.布尔检索

### 1.1信息检索概述

**结构化数据**

![image-20211230091357346](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300914154.png)

**非结构化数据**

*自由文本*

**允许:**

- 关键词 + 操作符
  - 奥运会 AND 游泳
- 更复杂的 概念性查询
  - 找出所有的有关药物滥用的网页

**半结构化数据**:

HTML

### 1.2倒排索引

![image-20211230092149781](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300921025.png)

#### 1.2.1 暴力方法

#### 1.2.2 关联矩阵

![image-20211230092443058](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300924218.png)

![image-20211230092603771](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300926990.png)

缺点:空间消耗大

#### 1.2.3 倒排索引

![image-20211230093216781](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300932950.png)

![image-20211230093425754](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300934984.png)

![image-20211230094211937](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300942146.png)

![image-20211230094351612](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300943870.png)

![image-20211230094524592](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300945825.png)

![image-20211230094922625](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300949811.png)

![image-20211230095054783](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300950972.png)

### 1.3词汇表和倒排记录表

![image-20211230095204093](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300952253.png)

![image-20211230095427946](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300954148.png)

![image-20211230095530972](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300955148.png)

![image-20211230095642738](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300956856.png)

![image-20211230095825898](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300958071.png)

![image-20211230095915226](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112300959420.png)

![image-20211230100011538](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301000687.png)

![image-20211230100051315](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301000578.png)

![image-20211230100228046](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301002205.png)

![image-20211230100521684](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301005839.png)

![image-20211230100718151](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301007333.png)

![image-20211230100822474](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301008650.png)

![image-20211230100838554](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301008753.png)

![image-20211230101129423](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301011605.png)

短语查询

![image-20211230101520877](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301015037.png)

![image-20211230101654527](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301016670.png)

![image-20211230101755578](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301017714.png)

![image-20211230101821912](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301018058.png)

临近搜索

![image-20211230102322649](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301023837.png)

## 小结

![image-20211230102539537](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301025698.png)

# 2.深度学习

![image-20211230152415117](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301524412.png)

![image-20211230154616007](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112301546690.png)

# 3.图形图像

图像就是矩阵

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312246265.png" alt="image-20211231224630025" style="zoom:33%;" />

## 主流颜色空间

- RGB
  - <img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312249851.png" alt="image-20211231224923708" style="zoom:50%;" />
  - <img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312250938.png" alt="image-20211231225013538" style="zoom:50%;" />
- 单通道灰度图 ->**减少运算**
  - <img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312248391.png" alt="image-20211231224839310" style="zoom:33%;" />

## 图像增强目的

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312250324.png" alt="image-20211231225055185" style="zoom:50%;" />

![image-20211231225213230](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312252371.png)

### **CLAHE** 常用技术

![image-20211231225411078](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312254284.png)

### 空间域图像增强

#### 滤波/卷积

![image-20211231225555302](https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312255398.png)

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312258048.png" alt="image-20211231225800858" style="zoom:50%;" />

 

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312307813.png" alt="image-20211231230754542" style="zoom:50%;" />

##### 中值滤波:(略)去噪用

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312308074.png" alt="image-20211231230857868" style="zoom:33%;" />

##### 高斯滤波:

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312310587.png" alt="image-20211231231043328" style="zoom:50%;" />

σ和滤波器决定清晰程度

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312312040.png" alt="image-20211231231243828" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312313752.png" alt="image-20211231231326596" style="zoom:50%;" />

##### 拉普拉斯滤波器:**增强对比**

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312313960.png" alt="image-20211231231354820" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312315467.png" alt="image-20211231231503230" style="zoom:50%;" />

### 高斯金字塔

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312318772.png" alt="image-20211231231829626" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312319250.png" alt="image-20211231231900935" style="zoom:50%;" />

#### 金字塔和高斯关系

**<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202112312353464.png" alt="image-20211231235312261" style="zoom:50%;" />**

**可以用小的高斯图像逐步还原原来图像**

##### haar小波变换 

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010106256.png" alt="image-20220101010601105" style="zoom:50%;" />

## 图像特征与描述

### 几何特征:斑点

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010112052.png" alt="image-20220101011211959" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010113283.png" alt="image-20220101011347073" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010114165.png" alt="image-20220101011430942" style="zoom:50%;" />

### 局部特征:SIFT

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010114674.png" alt="image-20220101011444560" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010119406.png" alt="image-20220101011948300" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010121279.png" alt="image-20220101012112134" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010122214.png" alt="image-20220101012229078" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010122520.png" alt="image-20220101012251376" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010123450.png" alt="image-20220101012305325" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010123180.png" alt="image-20220101012323052" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/img/202201010123933.png" alt="image-20220101012341742" style="zoom:50%;" />

