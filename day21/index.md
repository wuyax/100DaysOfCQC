#day21


## 校验码

码距: 从A码到B码转换，需要改变的位数成为码距。

## 奇偶校验码

检查错误，无法纠错。

## 循环冗余校验码CRC

只能检错，无法纠错。

计算->模2除法（模2除法与算术除法类似，但每一位除的结果不影响其它位，即不向上一位借位，所以实际上就是异或。）

生成多项式： g(x)=x^4+x^3+1 === g(x) = 1\*x^4+1\*x^3+0\*x^2+0\*x^1+1\*x^0 === 11001

## 海明码

第一步：求校验码的位数值K, 根据公式  2^k >= m+k +1

第二步：求校验码的位置   海明校验码方法中，校验码的位置是固定的，从2^0位，2^1 位 --> 2^2位  ... 2^n位 ,总个数为K位 

第三步：计算校验位的值
确定校验位的分组原则：每个位数都由R1、R2、R3中的一或若干个所确定。
R1校验的结果 1⊕1⊕1 = 1

R2校验的结果 1⊕0⊕1 = 0

R3校验的结果 1⊕0⊕1 = 0

[海明校验码--检错纠错详解](https://my.oschina.net/u/3374461/blog/1931270)