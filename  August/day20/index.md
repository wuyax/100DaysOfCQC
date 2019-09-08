#day20
细分知识点

## 进制转换

一、进制的表示  
二进制： 0b(binary)  
八进制：   
十进制：(decimal)  
十六进制： 0x/H(hexadecimal)  

二、二进制转换十进制    
使用**位权展开法**从低位到高位，每一位*2的位数次方。 
例如： 0b1100110  
转换：0\*2^0+1\*2^1+1\*2^2+0\*2^3+0\*2^4+1\*2^5+1\*2^6 = 102  

三、八进制转十进制  
道理和二进制转十进制一样只是把系数从二进制改为了八进制的位  

例如： 1577  
转换： 7\*8^0+7\*8^1+5\*8^2+1\*8# = 913  

四、十六进制转十进制
同理可得  
例如： 0x34EF
转换： f\*16^0+E\*16^1+4\*16^2+3\*163 = 13551

五、R进制转换为十进制   
例如： 53254
转换： 4\*R^0+5\*R^1+2\*R^2+3\*R^3+5\*R^4

六、十进制转R进制
十进制整数：使用**倒取余数法**用十进制整数除以R，记录每次所得余数，若商不为0则继续除以R，直到商位0，让后降所有余数从下至上记录，排列成从左到右的顺序，即为R进制数。
十进制小数：用十进制数乘以R，记录每次所得整数，若结果小数部分不为0，则将小数部分继续乘以R。直到没有小数，然后将所有小数从第一个开始从左至右依次排列，即为R进制数。

七、二进制转八进制
二进制数从地位到高位，每3为转换为对应的八进制即可，不够3位前面补0  
例如：0b1001001010  
转换：1112  

反过来：

例如： 645
转换： 0b110100101

八、二进制转十六进制
二进制数从地位到高位，每4为转换为对应的八进制即可，不够4位前面补0 
例如：0b1001001010  
转换：0x24A

反过来：

例如： 0xEF3
转换： 0b111011110011

九、任意进制之间互相转换
先转换为十进制，然后再转换为目标进制。

## 数的表示

各种数值再计算机中的表示形式成为机器数，以二进制表示，机器数对应的实际值成为真值。
无符号数：小数点在机器数的最低位之后则为纯整数，在最低位之前则为纯小数。  
带符号数：通过原码、反码、补码、移码表示。  

原码：

反码

补码：负数的补码等于他的原码自低位向高位，尾数的第一个‘1’及其右边的‘0’保持不变，左边的各位按位取反，符号位不变。

同余运算

## 浮点数的运算

N=F*2^E 
E为阶码 带符号的纯整数
F为尾数 带符号的纯小数

## 算术运算和逻辑运算
```
+ - * / 
```

```
&& || ! 异或 << 低位补0 >> 高位补0
```