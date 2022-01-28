# COA Review

[TOC]

## 导论

### 概念

* 冯氏结构工作方式

  预先存放到MEM、自动/逐条取指令并执行

* 冯氏结构的改进

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200109111745539.png" alt="image-20200109111745539" style="zoom:67%;" />

* 程序执行的过程

  - ⼯作⽅式
    - 采⽤存储程序的⽅式，程序和数据预先存放在存储器中
    - 机器⼯作时，⾃动、逐条地取出指令并执⾏
  - 程序执⾏
    - 顺序型：指令在存储器中按执⾏顺序存放，由指令计数器（PC）指明下⼀条指令的地址，⼀般按顺序递增
    - 转移型：根据运算结果或外界条件，改变下⼀条指令的地址

## 主存储器

### 概念

* SRAM和DRAM

  * 比较与应用

    ![image-20200108114740652](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114740652.png)

  * DRAM刷新

    ![image-20200108114305569](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114305569.png)

    * 集中式

      ![image-20200108114605467](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114605467.png)

    * 分散式

      ![image-20200108114634601](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114634601.png)

    * 异步式

      ![image-20200108114652064](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114652064.png)

    * 透明式

      ![image-20200108114709993](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108114709993.png)

* 编址方式

  * 顺序编制与交叉编址

    ![image-20200108113840389](C:\Users\Wong\AppData\Roaming\Typora\typora-user-images\image-20200108113840389.png)

    交叉编址的同一列可被同时选中

### 公式

- 存储容量

  ![image-20200108113416864](C:\Users\Wong\AppData\Roaming\Typora\typora-user-images\image-20200108113416864.png)



## 存储系统

### 概念

- 技术指标

  ![image-20200108115510242](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108115510242.png)

- 层次结构中的数据传递

  ![image-20200108120341820](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108120341820.png)

  ![image-20200108120355549](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108120355549.png)

  - 核心问题（实现）
    - 地址映射
    - 替换算法
    - 写策略

- Cache空间组织

  ![image-20200108131446311](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108131446311.png)

  ![image-20200108144350335](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108144350335.png)

  **Physic Address: Tag + Index + Byte-Offset**

- 虚拟存储空间

  - 段式

    ![image-20200108145402951](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108145402951.png)

    ![image-20200108145505815](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108145505815.png)

  - 页式

    ![image-20200108145605821](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108145605821.png)

    ![image-20200108145639643](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108145639643.png)

    **页式管理是基址寻址**：虚地址中给出虚页号+页表基址 ---> 页表中找实页号

  - 段页式

    ![image-20200108150018342](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108150018342.png)

    在页的基础上编段

  - 页表（PT）的组织

    ![image-20200108150757627](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108150757627.png)

  - 快表（TLB）的组织

    ![image-20200108150947464](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108150947464.png)

### 公式

* 带宽（衡量传输速度）

  ![image-20200108115440452](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108115440452.png)

* Cache性能指标

  ![image-20200108120727850](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108120727850.png)

* \* 辅助存储器的基本参数

  * 存储密度

    ![image-20200108151232109](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108151232109.png)

  * 存储容量

    ![image-20200108151303729](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108151303729.png)

  * 寻址时间

    ![image-20200108151337196](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108151337196.png)

  * 数据传输率

    ![image-20200108151406229](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108151406229.png)



## 指令集

### 概念

- 指令系统的要求

  ![image-20200108190901187](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108190901187.png)

- 各种字长

  ![image-20200108194342004](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108194342004.png)

- \* 数据与指令的存放、寄存器长度

  ![image-20200108194514429](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108194514429.png)

- 一些寻址方式的别名

  ![image-20200108203403350](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108203403350.png)

- 变址寻址

  ![image-20200108203439395](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108203439395.png)

  ![image-20200108203457107](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108203457107.png)

### 公式

### 方法

- 求解指令数![image-20200108193801568](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108193801568.png)

  设零地址$N_0$，单地址$N_1$，双地址$N_2$，则满足
  $$
  N_0 + N_1 \cdot 2^6 + N_2 \cdot 2^{12} = 2^{16}
  $$

## 中央处理器

### 概念

* \* 应用问题的产生与解决

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108205750077.png" alt="image-20200108205750077" style="zoom:67%;" />

* 四个基本操作

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108211346535.png" alt="image-20200108211346535" style="zoom:80%;" />

* 数据通路 - 哈佛结构

  ![image-20200108212025400](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108212025400.png)

* 时序信号

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108214231996.png" alt="image-20200108214231996" style="zoom:67%;" />

* 时序信号形成 - 变频

  ![image-20200108214839629](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108214839629.png)

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200108215051829.png" alt="image-20200108215051829" style="zoom:67%;" />

* 中断判断方法

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200109095701566.png" alt="image-20200109095701566" style="zoom:80%;" />

* CPU运行效率

  ![image-20200109101935003](D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200109101935003.png)

* 流水线性能

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200109110808942.png" alt="image-20200109110808942" style="zoom: 67%;" />

  <img src="D:\Documents\Lectures of Courses in SEU\Computor Organization and Architecture\Review\COA Review.assets\image-20200109110838701.png" alt="image-20200109110838701" style="zoom: 67%;" />

* 
