# 題目:What is the Probability?
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/0523ee03-262f-437a-a406-8586b9371e14)

# 程式碼:
````C++
#include <iostream>
#include <cmath>
#include <iomanip>
using namespace std;
int main(){
	int n,m;
	float p,q,k,w;
	cin>>n;
	while(n--){
		cin>>m>>p>>k;
		q=1-p;
		if(p==0.0){
			w=0;
		}
		else{
			w=pow(q,k-1)*p/(1-pow(q,m));
		}
		cout<<fixed<<setprecision(4)<<w<<endl;
	}
}
````
# 解題技巧:
待補
