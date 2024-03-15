# 題目:Can You Solve It?
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/a936164b-febc-46ab-839a-db275b2a5fac)
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/0719900e-1d7e-451e-8fae-2c5b857fac59)
# 程式碼
````C++
#include <iostream>
using namespace std;
int loc(int x,int y){
	return (x+y)*(x+y+1)/2+x;
}
int main(){
	int n,x1,y1,x2,y2,k=1;
	cin>>n;
	while(n--){
		cin>>x1>>y1>>x2>>y2;
		cout<<"Case "<<k++<<": "<<loc(x2,y2)-loc(x1,y1)<<endl;
	}
}
````
