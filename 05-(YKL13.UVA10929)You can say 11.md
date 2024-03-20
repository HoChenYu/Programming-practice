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

# 倍數判斷法(11的倍數)
國中的時候老師教過我們，要判斷N是否為11的倍數，可以用|奇數的總和-偶數的總和|取絕對值再去除以11若能整除代表該數N為11的倍數
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/da1d5810-1c88-4684-a290-4a41df4b00d2)
Reference: [台灣翰林](https://k12.xms.tw/media/427)

# 程式碼:
````C++
#include<iostream>
#include<cmath>
using namespace std;
int main(){
	string num;
	while(cin>>num){
		if(num=="0"){
			break;
		}
		else{
			int num2[2]={0,0};
			for(int i=0;i<num.size();i++){
				num2[i%2]=num2[i%2]+num[i]-'0';
			}
			if(abs(num2[0]-num2[1])%11==0)
			{
				cout<<num<<" is a multiple of 11."<<endl;
			}
			else{
				cout<<num<<" is not a multiple of 11."<<endl;
			}
		}
	}
}
````
