# Permutation
做项目的时候遇到了一个问题，需要从n个数组（元组）中各取一个元素，组成新的排列，这个排列中任何的重复元素都是没有用的。并没有很好的解决，但是已经基本上实现了我们想要的功能了。

## 现有方法

这段代码本来是一道比较经典的算法题，有很多种方法可以解决，比如直接对所有数组加起来做全排列，或者每个数组选一个数做，哪怕直接调用Python的函数直接算笛卡尔积都可以，网上有很多类似的资源。但是这些方法存在以下的问题：

### 复杂度过高

大部分只对较少的测试数据有用，当数据量很大的时候，就产生了时空复杂度过高的问题。比如说我们最开始遇到这个问题，就是因为32G的内存都吃不消MATLAB的那个perm()函数了。这促使我们下决心去优化。

### 重复数据

我们不需要排列中出现任何的重复数据，但是现有方法，在这样的情况下，都会有重复数据的产生，这些数据量不小，这也是造成复杂度过高的原因之一。

## 代码构成

有一个Java代码，网上找的，是现有方法，注释里面有一些的我自己的改动，但是改动不是很成功。

有一个C++代码，应该算是蛮好用的吧。

## 存在问题

因为数组的维数不知道怎么计算，我们每次都是手动测试的。少了会带来数据不全，多了会打印出一些奇奇怪怪的数字，应该是把内存里面别的东西也打印出来了。