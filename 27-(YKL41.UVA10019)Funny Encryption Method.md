# 題目:Funny Encryption Method
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/c26738c4-81d6-44f7-89be-f8ac9800a653)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int N,m;
	int hex[16]={0,1,1,2,1,2,2,3,1,2,2,3,2,3,3,4};
	cin>>N;
	while(N--){
		cin>>m;
		int b1=0,b2=0,m2=0;
		m2=m;
		while(m>0){
			b1+=m%2;
			m/=2;
		}
		while(m2>0){
			b2+=hex[m2%10];
			m2/=10;
		}
		cout<<b1<<" "<<b2<<endl;
	}
}
````
# 解題技巧:
對16進制的每一個數字做計算1的數量的統計，得出array[16]={0,1,1,2,1,2,2,3,1,2,2,3,2,3,3,4};
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f68e7db1-938b-4195-9b5d-4dc811e10e57)
