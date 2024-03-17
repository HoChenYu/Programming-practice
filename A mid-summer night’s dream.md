# 題目:A mid-summer night’s dream
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/334f6844-5ff6-48b5-b6f2-e973814aacf2)
# 程式碼:
````C++
#include <iostream>
#include <algorithm>
using namespace std;
int main(){
	int n,min,max,count;
	while(cin>>n){
		int a[n]={},sum[n]={};
		for(int i=0;i<n;i++){
			cin>>a[i];
		}
		sort(a,a+n);
		min=a[n/2];
		max=a[n/2];
		count=0;
		for(int i=0;i<n;i++){
			for(int j=0;j<n;j++){
				sum[i]+=abs(a[i]-a[j]);
			}
		}
		for(int i=0;i<n;i++){
			if(sum[i]==sum[n/2]){
				count++;
				if(a[i]<min){
					min=a[i];
				}
				if(a[i]>max){
					max=a[i];
				}
			}
		}
		cout<<min<<" "<<count<<" "<<max-min+1<<endl;
	}
}
````
# 解題技巧:
這題和vito family很類似，主要是找差的總和最小的值
輸出第一項是最小可能值，第二項是輸入資料中有幾項符合要求，第三項是這段區間內有多少數字符合需求
