# 題目:Fibonaccimal Base 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/82a5cd07-2519-4afc-9024-c1d28f5a19ac)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int N;
	cin>>N;
	int Fb[40]={0,1};
	for(int i=2;i<40;i++){
		Fb[i]=Fb[i-1]+Fb[i-2];
	}
	while(N--){
		int n,flag=0;
		cin>>n;
		cout<<n<<" = ";
		for(int i=40;i>=2;i--){
			if(n>=Fb[i]){
				n-=Fb[i];
				cout<<"1";
				flag=1;
			}
			else if(flag){
				cout<<"0";
			}
		}
		cout<<" (fib)"<<endl;
	}
}

````
# 解題技巧:
先把Fb[]這個array照規則排好，為什麼是[40]，因為題目測資
