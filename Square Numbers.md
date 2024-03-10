# 題目:Square Numbers
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/c9b6c37d-d323-4030-ac42-529f2154e05a)
# 程式碼:
````C++
#include <iostream>
#include <cmath>
using namespace std;
int main(){
	int a,b,n;
	while(cin>>a>>b){
		int count=0;
		if(a==0 and b==0){
			break;
		}
		for(int i=a;i<=b;i++){
			n=sqrt(i);
			if(n*n==i){
				count++;
			}
		}
		cout<<count<<endl;
	}
}
````
