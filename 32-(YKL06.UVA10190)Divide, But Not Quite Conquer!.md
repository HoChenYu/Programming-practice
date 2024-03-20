# 題目:Divide, But Not Quite Conquer! 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/c4b93bf4-5bd9-4bc2-986e-f4bf14a11155)
# 程式碼
````C++
#include <iostream>
#include <cmath>
#include <stack>
using namespace std;
int main(){
	long long a,b,count,cp;
	bool r=0;
	while(cin>>a>>b){
		r=0;
		count=0;
		cp=a;
		if(a==1||b==1||a<b){
			cout<<"Boring!"<<endl;
		}
		else{
		while(a>=b){
			if(a%b!=0){
				r=1;
				break;
			}
			a=a/b;
			count++;
		}
		if(r){
			cout<<"Boring!"<<endl;
		}
		else{
			for(int i=0;i<count;i++){
				cout<<cp<<" ";
				cp/=b;
			}
			cout<<"1"<<endl;
			}
		}
	}
}
````
