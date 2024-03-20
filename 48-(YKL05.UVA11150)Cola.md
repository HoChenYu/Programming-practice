# 題目:Cola
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/e0b0b6f0-506e-4aab-9aff-fe9dcde2d436)
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/b9a43fda-e00b-4738-9019-4be83cbe838a)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int n,count;
	while(cin>>n){
		count=0;
		while(n>=3){
			count+=3;
			n-=2;
		}
		if(n==2){
			count+=3;
		}
		else{
			count++;
		}
		cout<<count<<endl;
	}
}
````
# 解題技巧:
3個空瓶可以換1個，在n>=3時就一直喝，直到剩下兩個時(n==2)，題目說可以借1個空瓶所以先喝兩個湊三個空罐count+=3，剩下1個就直接喝
