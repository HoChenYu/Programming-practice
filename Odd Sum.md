# 題目:Odd Sum
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/20d42a73-de91-4724-a967-4f5951f1774c)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int m,count=0;
	cin>>m;
	while(m--){
		count++;
		int a,b,n;
		cin>>a>>b;
		if(a%2==0){
			a+=1;
		}
		if(b%2==0){
			b-=1;
		}
		n=(b-a+2)/2;
		cout<<"Case "<<count<<": "<<(a+b)/2*n<<endl;
	}
}
````
# 解題技巧
這題很簡單，就只是等差級數而已an=a0+(n-1)d
