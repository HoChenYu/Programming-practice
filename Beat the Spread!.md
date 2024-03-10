# Beat the Spread!
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/cc51291f-5e0c-4db0-8fc8-edb44692e2c4)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int n;
	cin>>n;
	while(n--){
		int s,d;
		cin>>s>>d;
		if(s<d || (s-d)%2){
			cout<<"impossible"<<endl;
		}
		else{
			cout<<(s+d)/2<<" "<<(s-d)/2<<endl;
		}
	}
}
````
# 解題技巧:
大的數字=(和+差)/2
小的數字=(和-差)/2
