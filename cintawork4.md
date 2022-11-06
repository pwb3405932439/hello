## CINTA作业四
### 第七章习题
#### 8.编程实现
```c++
#include<iostream>
#include<cmath>
#include<algorithm>
using namespace std;
int phi(int n) // 求欧拉函数
{
    int res=n;
    for(int i=2; i*i<= n; i++)
    {
        if (n%i==0)
            res = res/i*(i-1);
        while (n%i== 0)
            n/=i;
    }
    if(n>1)
        res=res/n*(n-1);
    return res;
}
int pow(int x, int y,int mod)//快速幂 
{
	int res = 1;
	while(y){
		if(y&1)res=(long long)res*x%mod;
		y>>=1;
		x=(long long)x*x%mod;
	}
	return res;
}	

int get_min(int m)//求最小生成元 
{
	int q[20001];
	int phiM=phi(m);
	q[0]=0;
	for(int i=2;i<phiM;i++)
		if(phiM%i==0)q[++q[0]]=i;
	for(int j=2;;j++)
	{
		bool flag=true;
		if(pow(j,phiM,m)!=1)continue;
		for(int i=1;i<=q[0];i++)
			if(pow(j,q[i],m)==1)
			{
				flag=false;
				break;
			}
		if(flag)return j;
	}
}
bool prime(int n)//判断是否是素数 
{
	for(int i=2;i<=sqrt(n);i++)
	{
		if(n%i==0)return false;
	}
	return true;
}
int main()
{
	int maxn=0,pos=0;
	for(int i=2;i<10000;i++)
	{
		if(!prime(i))continue;
		if(get_min(i)>maxn){
			maxn=get_min(i);
			pos=i;
		}
	}
	cout<<pos<<endl;//输出使最小生成元最大的素数 
    return 0;
}
```
