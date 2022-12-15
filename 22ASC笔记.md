##### 1.超级计算活动介绍（5分）

##### 2.微光团队介绍（5分）

##### 3.技术方案要求（90分）

###### 3.1.HPC系统设计（15分）

组装服务器

###### 3.2.HPL和HPCG（15分）

2.1 HPL
2.1.1 软件环境
操作系统：Centos7.2
编译器：mpiicc
数学库：MKL 2017
MPI 软件：MPICH-3.2.1
软件版本：HPL-2.2
2.1.2 测试方法
(1) 测试节点配置
使用单CPU节点，节点配置如下：
2 个 Intel E5-2683v3 处理器（28 核 2.0Gh2），
64GB DDR4 ECC REG 内存，
Infiniband QDR 40Gb/s 高速网络。
(2) 测试节点使用情况
每个核心分配一个进程，共28个进程，对应测试节点28个
核心。
(3) 作业提交方式
要使用 LSF 作业脚本向测试节点提交作业，LSF 作业脚本如下所示：

---

括软件环境的描述(操作系统、编译器、数学库、MPI软件、软件版本等)、性能优化和测试方法、性能测量、问题和解决方案分析等

**HPL**

>  HPL即High Performance Linpack，也叫高度并行计算基准测试，通过对高性能计算机采用高斯消元法求解一元N次稠密线性代数方程组的测试，评价高性能计算机的浮点性能。它对数组大小N没有限制，求解问题的规模可以改变，除基本算法（计算量）不可改变外，可以采用其他任何优化方法。
>
>   HPL是针对现代并行计算机提出的测试方法。用户在不修改任意测试程序的基础上，可以调节问题规模的大小（矩阵大小）、使用CPU数目、使用各种优化方法等等来执行该测试程序，以获得最佳的性能。HPL采用高斯消元法求解线性方程组。求解问题规模为N时，浮点运算次数为（2/3*N^3-2*N^2）。因此，只要给出问题规模N，测得系统计算时间T，峰值=计算量（2/3*N^3-2*N^2）/计算时间T，测试结果以浮点运算每秒（Flops）给出。

**HPCG**

> HPGC 高度共轭梯度基准测试, 是现在主要测试超算性能测试程序之一, 也是TOP500的一项重要指标.一般来讲HPCG的测试结果会比HPL低很多，常常只有百分几。

**Xeon**:至强是服务器的处理器

**Tesla:**Tesla，以发明家尼古拉·特斯拉的名字命名。它是一个新的显示核心系列品牌，主要用于伺服器高性能电脑运算，用于对抗AMD的流处理器。这是继GeForce和Quadro之后，第三个显示核心商标。NVIDIA将显示核心分为三大系列。GeForce系列是用来提供家庭娱乐；Quadro则用于专业缯图设计；Tesla用于大规模的并联电脑运算。

目前，Tesla有三个系列：

- Tesla GPU运算处理器 - 外形与普通显示卡大致相同，C870采用[GeForce 8](http://zh.wikipedia.org/zh-sg/GeForce_8)显示核心，而C1060采用[GeForce 200](http://zh.wikipedia.org/zh-sg/GeForce_200)显示核心，不设任何显示输出。
- Tesla GPU Deskside Supercomputer - 桌面平台用，外形与[QuadroPlex](http://zh.wikipedia.org/w/index.php?title=QuadroPlex&action=edit&redlink=1)相似，D870包含两张C870运算处理器，可透过接线互联多个装置。Tesla 10系列中没有相关产品。
- Tesla GPU Server - [服务器](http://zh.wikipedia.org/zh-sg/服务器)用，外形与1U伺服器相似，S870包含四张C870运算处理器，而S1070包含四张C1060运算处理器，可透过接线互联多个装置。

**操作系统**:

多数超级计算机使用操作系统为[Linux](https://so.csdn.net/so/search?q=Linux&spm=1001.2101.3001.7020)

**编译器**:

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/master/image-20220116194506056.png" alt="image-20220116194506056" style="zoom: 67%;" />

**数学库**:提供了科学计算所必须的cuBLAS线性代数库，cuFFT快速傅里叶变换库等,当深度学习大潮到来时，英伟达提供了cuDNN深度神经网络加速库

**MPI**:

MPI是一个库，而不是一门语言。但是按照并行语言的分类，可以把FORTRAN+MPI或者C+MPI看作是一种在原来串行语言基础上扩展后得到的并行语言。MPI库可以被FORTRAN77/C/FORTRAN90/C++调用，从语法上说，它遵守所有对库函数/过程的调用规则，和一般的函数/过程没有什么区别。

MPI是一种标准或规范的代表，而不特指某一个对它的具体实现。迄今为止，所有的并行计算机制造商都提供对ＭＰＩ的支持，可以在网上免费得到ＭＰＩ在不同并行机上的实现。一个正确的ＭＰＩ程序，可以不加修改地再所有的并行机上运行。 

ＭＰＩ是一种消息传递编程模型，并成为这种编程模型的代表和标准。

消息传递方式是广泛应用于多类并行机的一种模式,特别是那些分布存储并行机，尽管在具体的实现上有许多不同,但通过消息完成进程通信的基本概念是容易理解的。十多年来，这种模式在重要的计算应用中已取得了实质进步。有效和可移植地实现一个消息传递系统是可行的，因此，通过定义核心库程序的语法、语义，这将在大范围计算机上可有效实现将有益于广大用户。这是MPI产生的重要原因。  

*MPI的目的：较高的通信性能，较好的程序可移植性，强大的功能。*

**软件编程:**CUDA编程模型,软件开发人员从此可以使用CUDA在英伟达的GPU上进行并行编程.CUDA对于GPU就像个人电脑上的Windows、手机上的安卓系统，一旦建立好生态，吸引了开发者，用户非常依赖这套软件生态体系。GPU编程可以直接使用CUDA的C/C++版本进行编程，也可以使用其他语言包装好的库，比如Python可使用Numba库调用CUDA。CUDA的编程思想在不同语言上都很相似。

CUDA及其软件栈的优势是方便易用，缺点也显而易见：

1. 软件环境复杂，库以及版本很多，顶层应用又严重依赖底层工具库，入门者很难快速配置好一整套环境；多环境配置困难。
2. 用户只能使用英伟达的显卡，成本高，个人用户几乎负担不起。

因此，如果没有专业的运维人员维护GPU机器，最好还是在公有云上按需购买GPU虚拟机。入门者可以考虑云厂商的Telsa P4虚拟机，大约10+元/小时，云厂商会配置好CUDA及工具库。

CUDA:

<img src="C:\Users\syc\AppData\Roaming\Typora\typora-user-images\image-20220114192613937.png" alt="image-20220114192613937" style="zoom:50%;" />

<img src="C:\Users\syc\AppData\Roaming\Typora\typora-user-images\image-20220114193027105.png" alt="image-20220114193027105" style="zoom:50%;" />

**CUDA+MPI:**

针对大数据的计算，很多程序通过搭建mpi集群进行加速，并取得了很好的效果。算法内部的加速，当前的并行化趋势是利用GPU显卡进行算法加速。针对并行性非常好的算法，GPU加速效果将远大于集群带来的加速效果。所以，如果我们面临非常多的数据，针对数据的处理算法有具有很好的内部并行性，则我们可以将mpi和GPU结合，获得更大的加速比。

**其他超算平台:**



<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/master/image-20220116194147409.png" alt="image-20220116194147409" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/master/image-20220116194201458.png" alt="image-20220116194201458" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/master/image-20220116194210516.png" alt="image-20220116194210516" style="zoom:50%;" />

<img src="https://gitee.com/yonaspigeon/giteepicstore/raw/master/master/image-20220116194222108.png" alt="image-20220116194222108" style="zoom:50%;" />



###### 3.3.袁大型语言模型挑战赛（30分）

简单地说，语言模型就是用来计算一个句子的概率的模型，也就是判断一句话是否是人话的概率？

我们只要求参与者在尽可能短的时间内完成10 亿代币的训练，达到损失值小于7.0

所提交的培训前日志文件需要包括以下内容： 

​	a)所有超参数，包括模型结构参数、随机种子、批处理大小、学习率等。 

​	b)模型训练的开始和结束时间 

​	c)每个迭代步骤的信息，包括batch_size、learning_rate、每次迭代期间的损失和时间成本

###### 3.4.DeePMD挑战（30分）

