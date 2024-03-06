# 題目:Vito'sfamily
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/d9980a47-45ff-4b5b-9bc1-4b4829ada634)

# 錯誤程式碼:
````C++
#include <iostream>
#include <algorithm>
#include <cmath>
using namespace std;
int main(){
	int n;
	while(cin>>n){
		int s[501];
		int m,total;
		cin>>m;
		for(int i=0;i<m;i++){
			cin>>s[i];
		}
		sort(s,s+m);
		total=0;
		for(int i=0;i<m;i++){
			total+=abs(s[i]-s[m/2]);
		}
		cout<<total<<endl;
		n--;
	}
}
````
# 正確程式碼:
````C++
#include <iostream>
#include <algorithm>
using namespace std;
int main(){
	int n;
	cin>>n;
	while(n--){
		int m,i,a[100000];
		cin>>m;
		for(i=0;i<m;i++){
			cin>>a[i];
		}
		sort(a,a+m);
		int sum=0;
		for(i=0;i<m;i++){
			sum+=abs(a[i]-a[m/2]);
		}
		cout<<sum<<endl;
	}
}	
````
