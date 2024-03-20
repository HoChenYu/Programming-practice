# 題目:Summing Digits
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f0058f4f-148c-475a-8723-0bd36b5000f4)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int n,last;
	while(cin>>n,n!=0){
		while(n>=10){
			last=0;
			while(n){
				last+=n%10;
				n/=10;
			}
			n=last;
		}
		cout<<n<<endl;
	}
}
````
