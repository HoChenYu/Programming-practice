# 題目:2 the 9s.md
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/1ac6abe6-12e2-43eb-ab54-c788356d4e47)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	string s,a;
	while(cin>>s,s!="0"){
		int sum=0;
		int count=1;
		for(int i=0;i<s.size();i++){
			sum+=s[i]-'0';
		}
		if(sum%9!=0){
			cout<<s<<" is not a multiple of 9."<<endl;
		}
		else{
			cout<<s<<" is a multiple of 9 and has 9-degree ";
			a=to_string(sum);
			while(a.size()>1){
				sum=0;
				for(int i=0;i<a.size();i++){
					sum+=a[i]-'0';
				}
				a=to_string(sum);
				count++;
			}
			cout<<count<<"."<<endl;
		}
	}
}
````
