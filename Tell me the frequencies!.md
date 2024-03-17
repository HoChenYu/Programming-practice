# 題目:Tell me the frequencies!
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/87cac3d8-b524-428b-bd80-9dea974e0eab)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	string s;
	int count=1;
	while(getline(cin,s)){
		if(count!=1){
		cout<<endl;}
		int a[200]={};
		for(int i=0;i<s.size();i++){
			a[s[i]-'0'+48]++;
		}
		for(int j=1;j<=s.size();j++){
			for(int i=200;i>0;i--){
				if(a[i]==j){
					cout<<i<<" "<<a[i]<<endl;
				}
			}
		}
		count++;
	}
}
````
