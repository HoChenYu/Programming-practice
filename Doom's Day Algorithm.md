# 題目:Doom's Day Algorithm
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/1462761e-635f-4bc3-a594-9f0d0426f38e)

# 程式碼:
````C++
#include <iostream>
#include <cmath>
using namespace std;
int main(){
	int n,M,D,num;
	int month[]={0,31,59,90,120,151,181,212,243,273,304,334};
	string day[]={"Friday","Saturday","Sunday","Monday","Tuesday","Wednesday","Thursday"};
	cin>>n;
	while(n--){
		cin>>M>>D;
		num=month[M-1]+D;
		cout<<day[num%7]<<endl;
	}

}
````

# 解題技巧:
雖然這題很簡單可以用暴力做法，但很顯然不夠聰明  
我們可以先換算成現在是一年的第幾天，這樣我們只要知道1/1是星期幾剩下的取餘數就能求得了  
ex:該題1/1是星期六(%7==1)，代表%7==0的就是禮拜五，依此類推
