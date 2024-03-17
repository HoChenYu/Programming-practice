# 題目:Train Swapping
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/2b5e7147-d255-4cbc-96ec-eae794457ef5)
# 程式碼
````C++
#include <iostream>
using namespace std;
int main(){
	int n1,n2,tmp;
	cin>>n1;
	while(n1--){
		int count=0;
		cin>>n2;
		int a[n2]={};
		for(int i=0;i<n2;i++){
			cin>>a[i];
		}
		for(int j=0;j<n2;j++){
		for(int i=0;i<n2-j-1;i++){
			if(a[i]>a[i+1]){
				tmp=a[i];
				a[i]=a[i+1];
				a[i+1]=tmp;
				count++;
			}
		}
		}
		cout<<"Optimal train swapping takes "<<count<<" swaps."<<endl;
	}	
}
`````
# 解題技巧
計算bubble sort 次數
