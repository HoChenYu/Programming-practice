# 題目:Satellites
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/8537b9c4-e738-4520-9a3a-ffcb61d172be)
# 程式碼:
````C++
#include <iostream>
#include <iomanip>
#include <cmath>
#define _USE_MATH_DEFINES
using namespace std;
int main(){
	double s,a,b;
	string str;
	while(cin>>s>>a>>str){
		if(str[0]=='m'){
			a/=60;
		}
		s+=6440;
		b=a*M_PI/180;
		cout<<fixed<<setprecision(6)<<2*s*M_PI*a/360<<" "<<2*s*sin(b/2)<<endl;
	}
	return 0;
}
````
# 解題技巧
困難在使用函式庫和min=60*deg，這一般人根本不會知道A_A  
使用setprecision(n)前一定要加上fixed，並且引用````<iomanip>````  
使用M_PI要引用<cmath>且定義_USE_MATH_DEFINES  
sin()是使用弧度而不是角度  
180度=PI so 1弧度=PI/180
