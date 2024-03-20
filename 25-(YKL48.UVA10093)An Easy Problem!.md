# 題目:An Easy Problem!
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/6f8b5df1-9308-4632-b8d9-2a4ffcd17e45)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int max,sum;
	string s;
	while(cin>>s){
		max=1;
		sum=0;
		for(int i=0;i<s.size();i++){
			int d=0;
			if(s[i]>='0' && s[i]<='9'){
				d=s[i]-'0';
			}
			if(s[i]>='A' && s[i]<='Z'){
				d=s[i]-'A'+10;
			}
			if(s[i]>='a' && s[i]<='z'){
				d=s[i]-'a'+36;
			}
			sum+=d;
			if(d>max){
				max=d;
			}
		}
		int r;
		for(r=max+1;r<=62;r++){
			if((sum%(r-1))==0){
				break;
			}
		}
		if(r<=62){
			cout<<r<<endl;
		}
		else{
			cout<<"such number is impossible!"<<endl;
		}
		
	}
}
````
# 解題技巧:
r的範圍 數字0~9(10位) A~Z(26位) a~Z(26位) 總共62位
