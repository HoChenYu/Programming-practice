# 題目:3n+1problem
<img width="575" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/fff250a1-e437-4fa9-8ca0-e21e6472c2ca">

# 程式碼:
````C++
#include <iostream>
#include <cmath>
using namespace std;
bool oddornot(int n){
	if(n%2==1){return true;}
	else
		return false;
}
int cyclelength(int n){
	int length=0;
	while(n){
	length+=1;
	//cout<<"n:"<<n<<"length:"<<length<<endl;
	if(n==1){break;}
	else if(oddornot(n)){
		n=3*n+1;}
	else{
		n=n/2;}
	}
	return length;
}
int main(){
	int a,b;
	while(cin>>a>>b){
		int max=0;
		cout<<a<<" "<<b<<" ";
		int tmp;
		if(a>b){
			tmp=b;
			b=a;
			a=tmp;
		}
		for(int i=a;i<=b;i++)
		{
			if(cyclelength(i)>max)
			{max=cyclelength(i);}
		}
		cout<<max<<endl;
	}
	return 0;
}
````
