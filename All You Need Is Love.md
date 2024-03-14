# 題目:All You Need Is Love 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/2ac79793-d625-425d-a850-818d873fd7cc)
# 程式碼:
````C++
#include <iostream>
#include <algorithm>
#include <cmath>
using namespace std;
long long twototen(string s){
	int n=0;
	for(int i=s.size()-1;i>=0;i--){
		n=n+(s[i]-'0')*pow(2,s.size()-i-1);
	}
	return n;
}
int main(){
	int N,count=1;
	string s1,s2;
	long long a1,a2;
	cin>>N;
	while(N--){
		cin>>s1>>s2;
		a1=twototen(s1);
		a2=twototen(s2);
		if(__gcd(a1,a2)==1){
			cout<<"Pair #"<<count<<": Love is not all you need!"<<endl;
		}
		else{
			cout<<"Pair #"<<count<<": All you need is love!"<<endl;
		}
		count++;
	}
}
````
# 解題技巧:
從S1和S2中找出一個S能構成這兩個string，11011(s1)-11(L)=11000(s2)  
也就是說S1和S2轉換成十進位之後會有一個最大公因數
