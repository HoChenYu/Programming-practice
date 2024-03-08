# 題目:
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/1684bc4e-813b-47ad-a2ac-1349dc67bb28)

#程式碼:
````C++
#include <iostream>
#include <cmath>
using namespace std;
bool checkfun(int n[],int m){
	for (int i=1;i<=m-1;i++){
		if(n[i]!=1){
			return false;
		}
	}
	return ture;
}
int main(){
	int n;
	int set[3000];
	while(cin>>n){
		if(n==1){
		cin>>set[0];
		cout<<"Jolly"<<endl;}
		else{
		int check[3001]={};
		for(int i=0;i<n;i++){
			cin>>set[i];
		}
		for(int i=0;i<n-1;i++){
			check[abs(set[i]-set[i+1])]=1;
		}
		if(checkfun(check,n)){
			cout<<"Jolly"<<endl;
		}
		else{
			cout<<"Not jolly"<<endl;
		}
		}	
	}
}
````

# 解題技巧:
在while回圈內創建一個負責檢查的array，一定要在while內創建並初始化，因為每次要檢查的結果都不一樣!
如果要寫在while外，在while內就必須fill(begin(check), end(check), 0);
