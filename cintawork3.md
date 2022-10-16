## CINTA作业三
### 1.设*p=23,a=3*，使用费尔马小定理计算*a<sup>2019</sup> mod p*.
3<sup>2019</sup> mod p = 3<sup>91 x (23-1)+17</sup> = 3<sup>17</sup>  = 16 (mod 23) 

### 2.使用费尔马小定理求解同余方程x<sup>50</sup> $\equiv$ 2 (mod 17)
x<sup>50</sup> $\equiv$ 2 (mod 17) </br> x<sup>16x3+2</sup> $\equiv$ 2 (mod 17) </br> x<sup>2</sup> $\equiv$ 2 (mod 17)  
令1 $\leqslant$ x $\leqslant$ 17,将1...17代入上式计算得:  
x<sub>1</sub>=6 , x<sub>2</sub>=11  
综上，当x=6或11，x<sup>50</sup> $\equiv$ 2 (mod 17)成立

### 5.请证明13整除2<sup>70</sup>+3<sup>70</sup>.  
  2<sup>70</sup>+3<sup>70</sup> (mod 13)   
= (2<sup>70</sup> mod 13 + 3<sup>70</sup> mod 13) mod 13  
= (2<sup>5x12+10</sup> mod 13 + 3<sup>5x12+10</sup> mod 13) mod 13  
= (2<sup>10</sup> mod 13 + 3<sup>10</sup> mod 13) mod 13  
= (4<sup>4</sup>x4 mod 13+(-4)<sup>4</sup>x9 mod 13) 2<sup>70</sup>+3<sup>70</sup>mod 13  
= 4<sup>4</sup>x(4+9) mod 13
= 4<sup>4</sup>x13 mod 13  
= 0 mod 13  
所以13整除2<sup>70</sup>+3<sup>70</sup>。

### 6.使用欧拉定理计算2<sup>100000</sup> mod 55
