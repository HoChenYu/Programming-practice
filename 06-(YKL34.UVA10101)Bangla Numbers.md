# 題目:Bangla Numbers

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/3d3da31c-cda5-44f4-83f5-ea33585d010b)
# 程式碼
````C++
#include <iostream>
#include <iomanip>
using namespace std;
int Bangla(long long n){
	if(n>=10000000){
		Bangla(n/10000000);
		cout<<" kuti";
		n%=10000000;
	}
	if(n>=100000){
		cout<<" "<<n/100000<<" lakh";
		n%=100000;
	}
	if(n>=1000){
		cout<<" "<<n/1000<<" hajar";
		n%=1000;
	}
	if(n>=100){
		cout<<" "<<n/100<<" shata";
		n%=100;
	}
	if(n){
		cout<<" "<<n;
	}
}
int main(){
	long long n;
	int count=1;
	while(cin>>n){
		cout<<setw(4)<<count<<".";
		Bangla(n);
		count++;
		if(n==0){cout<<" 0";}
		cout<<endl;
	}
	return 0;
}
````
# 解題技巧
````C++
#include <iomanip>
````
引用補空白的header
