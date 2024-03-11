# 題目:GCD
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/2f2f9c96-eac7-4c5a-81af-f16b866576c8)

# 程式碼:
````C++
#include <iostream>
#include <algorithm>
using namespace std;
int main(){
	int n;
	while(cin >> n,n!=0){
		int i,j,g=0;
		for(i=1;i<n;i++){
			for(j=i+1;j<=n;j++) g+=__gcd(i,j);
		}
		cout << g << endl;
	}
}
````
