# 題目:Simply Emirp 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f045f3e8-ba47-4a91-b5fe-6bce1338ac49)
# 程式碼:
````C++
#include <iostream>
#include <algorithm>
using namespace std;
bool prime(int n){
	for(int i=2;i<n;i++){
		if(__gcd(n,i)!=1){
			return false;
			break;
		}
	}
	return true;
}
int stringtoint(string s){
	int n=0;
	for(int i=0;i<s.size();i++){
		n*=10;
		n+=(s[i]-'0');
	}
	return n;
}
int stringtoint2(string s){
	int n=0;
	for(int i=s.size()-1;i>=0;i--){
		n*=10;
		n+=(s[i]-'0');
	}
	return n;
}
int main(){
	string n;
	int a,b;
	while(cin>>n){
		a=stringtoint(n);
		b=stringtoint2(n);
		if(!prime(a)){
			cout<<a<<" is not prime."<<endl;
		}
		else{
			if(a==b){
				cout<<a<<" is prime."<<endl;
			}
			else if(prime(b)){
				cout<<a<<" is emirp."<<endl;
			}
			else{
				cout<<a<<" is prime."<<endl;
			}
		}
	}
}
````
# 解題技巧:
用字串來存，左移就是乘以十，透過GCD看最大公因數如果不是1代表他不是質數
