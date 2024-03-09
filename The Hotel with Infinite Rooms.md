# 題目:The Hotel with Infinite Rooms
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/7d6819c0-f0ad-407f-aeba-1d0f9a4d4bd2)
# 程式碼:
````
#include <iostream>
using namespace std;
int main(){
	int s;
	long long D;
	while(cin>>s>>D){
		while(s<D){
			D-=s;
			s++;
		}
		cout<<s<<endl;
	}
}
````
# 解題技巧:
第一天有s個，找第D天人數
(s,D)=(s+1,D-S)直到s>D，因為題目有說s人會待s天，所以做到s>D就可以停下來了
