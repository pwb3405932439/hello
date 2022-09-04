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
