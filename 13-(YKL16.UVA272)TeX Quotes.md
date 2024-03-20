# 題目:TeX Quotes 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/5bab213c-d004-4a1f-817c-64afd5f66060)
# 範例input&output
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/65b86291-0a00-42c6-a2f5-5318c95735d9)
# 程式碼
````C++
#include <iostream>
#include <string>
using namespace std;
int main(){
	char n;
	string a;
	int i=0;
	int count;
	while(cin.get(n)){
		if(n=='"'){
			count++;
			if(count%2){
				cout<<"``";
			}
			else{
				cout<<"''";
			}
		}
		else{
			cout<<n;
		}
	}
	
}
````
