# 題目:Symmetric Matrix 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/a8864b0d-767d-49c1-a6a1-a52ba8c5c7c7)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int n,t,count=0;
	string r;
	cin>>n;
	while(n--){
		count++;
		int check=1;
		cin>>r>>r>>t;
		int a[t*t]={};
		for(int i=0;i<t*t;i++){
			cin>>a[i];
		}
		for(int i=0;i<t*t;i++){
			if(a[i]<0 or a[i]!=a[t*t-1-i]){
				check=0;
				break;
			}
		}
		if(check){
		cout<<"Test #"<<count<<": Symmetric."<<endl;
		}
		else{
		cout<<"Test #"<<count<<": Non-symmetric."<<endl;
		}
	}
	return 0;
}
````
# 解題技巧
關鍵在於第i個元素，正方形矩陣寬度T的情況
a[i]應該要等於a[T*T-1-i]，減去1是因為i從0開始
