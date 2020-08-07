# Chapter 1

## 环境 工具 IDE

- [安装 java](https://lift.cs.princeton.edu/java/linux/)
- [安装 命令行工具](https://lift.cs.princeton.edu/java/linux/)
  - 安装完工具之后我们就可以使用`javac-algs4`和`java-algs4`这两个工具,这两个工具已经导入本书所需的标准库`stdlib.jar`,我们可以直接使用
- [安装 IntelliJ](https://lift.cs.princeton.edu/java/linux/)

## stdlib

在这本书中,作者已经预先完成一些`I/O`库,这些库比标准库有更多的功能,很好的输出展示方式,更智能的输入控制,我们有多种方式来使用,推荐的两种方式:

1. 使用`javac-algs4`和`java-algs4`命令行
2. 使用 `IntelliJ`编辑器添加依赖库`File --> Project Struct --> 点击 + 选择 Java -->选择 stdlib.jar 在本地的路径`

## 1.5 union-find

### 1.5.1 我的想法

看完138页之后我的想法
使用数组来存储各个触点,我认为多个触点组成一个联通分量的时候,可以使用下标最小的那个触点作为`分量标识符`,其他触点都将值置为这个触点的下标值.当连接两个触点的时候,需要判断
触点值是否是同个下标,是的话说明这两个分量是联通的.如果不是同一联通分量,遍历数组将`分量标识符`为较大值的分量中所有触点的值改成较小的那个`分量标识符`.

quick-union vs 加权 quick-union

加权