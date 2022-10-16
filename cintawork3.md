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
由 $\phi$ (55)=40得:  
2<sup>100000</sup> mod 55  
= 2<sup>2500x40</sup> mod 55  
= 1 (mod 55)  

### 8.手动计算7<sup>1000</sup>的最后两个数位等于什么
解答：7<sup>1000</sup>的最后两个数位是01；  
由$\phi$(100)=40得: 7<sup>1000</sup> mod 100 $\equiv$ 7<sup>40x25</sup> mod 100 $\equiv$ 1 mod 100 

### 10.设p是素数，计算(p-1)！mod p ,并找出规律，写成定理，并给出证明。
p=2, (2-1)! mod 2 $\equiv$ 1 mod 2;  
p=3, (3-1)! mod 3 $\equiv$ 2 mod 3;  
p=5, (5-1)! mod 5 $\equiv$ 4 mod 5;  
所以(p-1)！mod p $\equiv$ (p-1) mod p;  
证明如下:
1) 1 mod p $\equiv$ 1 mod p;
2) (p-1)<sup>2</sup> mod p $\equiv$ 1 mod p;
3) 对于任意一个m属于1...(p-1), 必定存在唯一一个逆元n属于1...(p-1)使得mn mod p $\equiv$ = 1 mod p  
   因为p是素数，所以1...(p-1)中有偶数个整数，2...(p-2)中也有偶数个整数  
   所以2...(p-2)中的数能构成一定数量的数对(m,n),其中gcd(m,n)=1且m,n都属于2...(p-2)  
   (p-2)(p-3)(p-4)...2 mod p $\equiv$ 1 mod p

综上所述，  
(p-1)！mod p $\equiv$ (p-1) mod p
   
