## CINTA作业二
### 7、
``` c++
#include <iostream>
using namespace std;
bool judge(int n)
{
	if(n%2==0)return true;
	else return false;
}
int main()
{
	int n;
	cin>>n;
	if(judge(n))cout<<"True."<<endl;
	else cout<<"False."<<endl;
	return 0;
}
```
### 8、
``` c++
#include <iostream>
using namespace std;
int ans(int x,int y,int m)
{
	int counter=1;
	while(y)
	{
		if(y%2==1){
			counter=(counter*x)%m;
		}
		y=y>>1;
		x=(x*x)%m;
	}
	return counter;
}
int main(){
	int x,y,m;
	cin>>x>>y>>m;
	cout<<ans(x,y,m)<<endl;
	
	return 0;
}
```
### 9、
``` c++
#include <bits/stdc++.h>
using namespace std;
int a[2][2];
void mult(int a[][2],int b[][2])
{
	int c[2][2];
	 memset(c,0,sizeof c);
    for(int i = 0; i < 2; i++){
        for(int j = 0; j < 2; j++){
            for(int k = 0; k < 2; k++){
                c[i][j] = c[i][j] + a[i][k] * b[k][j];	
            }
        }
    }
    for(int i = 0; i < 2; i++){
        for(int j = 0; j < 2; j++){
            a[i][j] = c[i][j];
        }
    }
}
void mult_pow(int a[][2],int n)
{
	int unit[2][2];
	for(int i=0;i<2;i++)
		for(int j=0;j<2;j++){
			if(i==j)unit[i][j]=1;
			else unit[i][j]=0;
		}
	while(n){
		if(n % 2==1)mult(unit,a);
		mult(a,a);
		n=n>>1;
	}
	for(int i = 0; i < 2; i++){
        for(int j = 0; j < 2; j++){
            a[i][j] = unit[i][j];
        }
    }
}
int main(){
	a[0][0]=a[0][1]=a[1][0]=1;
	a[1][1]=0;
	int n;
	cin>>n;
	mult_pow(a,n);
	cout<<a[0][1]<<endl;
}
```
### 10、
存在性：  
因为正整数c和m是互素的，所以gcd(c,m)=1，则c必然存在mod m的意义上的乘法逆元；
 
唯一性：
假设c在mod m意义上有存在两个不相等的逆元：b<sub>1</sub>和b<sub>2</sub> 且 b<sub>1</sub> $>$ b<sub>2</sub>;
那么一定有:  
 $$ c*b<sub>1</sub>=c*b<sub>2</sub>= k ($mod$ m)
所以c*b<sub>1</sub>=q<sub>1</sub>m+k,c*b<sub>2</sub>=q<sub>2</sub>m+k;  
由上式相减得：c*(b<sub>1</sub>-b<sub>2</sub>)=(q<sub>1</sub>-q<sub>2</sub>)m;  
两边同时 $mod$ m:   
等式左边=c*(b<sub>1</sub>-b<sub>2</sub>) $mod$ m;  
等式右边=(q<sub>1</sub>-q<sub>2</sub>)m $mod$ m=0;  
又因为gcd(c,m)=1,所以b<sub>1</sub>-b<sub>2</sub>一定等于0,与假设矛盾。  
    
综上，在 $mod$ m 的意义上存在唯一确定的整数值c<sup>-1</sup>,它使得 $cc<sup>-1</sup> = (mod m)$ .
