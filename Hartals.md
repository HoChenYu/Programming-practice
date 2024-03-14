# 題目:Hartals
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/1a4d92ba-511d-44ad-8a31-c62ac71207d0)
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/4549108c-84d7-41b8-a63d-7cd435622060)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int T,N,n,h;
	cin>>T;
	while(T--){
		cin>>N;
		int worklist[N]={},count=0;
		cin>>n;
		for(int i=0;i<n;i++){
			cin>>h;
			for(int j=1;j<=(N/h);j++){
				worklist[j*h-1]=1;
			}
		}
		for(int i=0;i<N;i++){
			if(i%7==5||i%7==6){
				worklist[i]=0;
			}
			else if(worklist[i]){
				count++;
			}
		}
		cout<<count<<endl;
	}
}
````
# 解題技巧:
把一個禮拜中會有派對的那幾天在array上設值為1，之後在將mod5或6的值設為0，其餘worklist[i]為true時count++
