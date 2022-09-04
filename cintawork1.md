## CINTA作业一
### 1、
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
### 2、
``` c++
#include <iostream>
using namespace std;
bool judge(int n)
{
	if(n<=0)return false;
	if((n&(n-1))==0)
		return true;
	else 
		return false;
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
### 3、
``` c++
#include <iostream>
using namespace std;
int multiply(int a,int b)
{
	if(a==0||b==0)return 0;
	if(b%2==0)return 2*multiply(a,b/2);
	else return 2*multiply(a,b/2)+a;
 } 
int main()
{
	int a,b;
	cin>>a>>b;
	cout<<a<<" x "<<b<<" = "<<multiply(a,b);
	return 0;
}
```
### 4、
由a|b得：b=q<sub>1</sub>a;    
由b|c得：c=q<sub>2</sub>b;  
因为c=q<sub>2</sub>b=q<sub>2</sub>q<sub>1</sub>a, $~$所以c=q<sub>3</sub>a;  
由c=q<sub>3</sub>a得：c|a.  
  
如果c|a，则a=q<sub>1</sub>c;  
如果c|b，则b=q<sub>2</sub>c;  
对于任意m和n，ma+nb=mq<sub>1</sub>c+nq<sub>2</sub>c=(mq<sub>1</sub>+nq<sub>2</sub>)c=q<sub>3</sub>c;  
因为ma+nb=q<sub>3</sub>c，所以有c|(ma+nb).
### 7、
假设形如 111 · · · 111的整数中存在一个整数是某个数的平方数，设该整数数为a<sup>2</sup>，则a<sup>2</sup>-1=(a+1)(a-1);  
又因为只有尾数为9或1的数的平方才会得到尾数为1的整数，所以a为奇数，(a+1)和(a-1)为偶数；  
因为(a+1)和(a-1)都可以被2整除，所以a<sup>2</sup>-1可以被4整除；  
又因为任意形如 111 · · · 111的整数减1后无法被4整除，所以任意形如 111 · · · 111的整数都不是平方数.
