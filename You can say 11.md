# 題目:You can say 11.
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/5dbf7c01-5115-4135-acbc-930aeb8afb06)

# 錯誤程式碼:
很顯然沒注意到1000digits
````C++
#include<iostream>
using namespace std;
int main(){
	long long num;
	while(cin>>num){
		if(num%11==0){
			cout<<num<<" is a multiple of 11."<<endl;
		}
		else{
			cout<<num<<" is not a multiple of 11."<<endl;
		}
	}
}
````
