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
