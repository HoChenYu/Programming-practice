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
#include <cmath>
using namespace std;
int main(){
	int n;
	cin>>n;
	while(n--){
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
	}
}
````
# 錯誤檢討

練了一陣子還是有這種低級錯誤... 

while內放入cin>>只要>0恆true，換句話說while(cin>>n)即便在迴圈最後寫上n--都是沒有意義的，因為下次會輸入新的值
