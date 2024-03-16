# 題目:Fourth Point!! 
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f4e2a2a3-d4da-47d9-94e6-223c398440f0)
# 程式碼:
````c++
#include <iostream>
#include <iomanip>
using namespace std;
int main(){
	double x,y,x1,x2,x3,x4,y1,y2,y3,y4;
	while(cin>>x1>>y1>>x2>>y2>>x3>>y3>>x4>>y4){
		x=x1+x2+x3+x4;
		y=y1+y2+y3+y4;
		if((x1==x3&&y1==y3)||(x1==x4&&y1==y4)){
			x-=3*x1;
			y-=3*y1;
		}
		else{
			x-=3*x2;
			y-=3*y2;
		}
		cout<<fixed<<setprecision(3)<<x<<" "<<y<<endl;
	}
}
````
# 解題技巧:
因為一開始輸入是兩個鄰邊的點，是3+1重複，選第一個鄰邊來看，要馬是(X1,Y1)重複，要馬是(X2,Y2)重複  
因此透過求得平行四邊形公式對角的座標相加除以二，為了找出第四個座標，推導出三個點相加起來後，扣掉三倍找出重複的點(X1,Y1)
