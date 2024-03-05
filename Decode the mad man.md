# 題目:Decode the mad man

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/1f4c6d97-03a9-4725-b55d-e9c610e239ed)

# 程式碼: 

````C++
#include <iostream>
#include <cstring>
using namespace std;
int main(){
	char n;
	char s[]="1234567890-=qwertyuiop[]\\asdfghjkl;'zxcvbnm,./";
	while(cin.get(n)){
		n=tolower(n);
		char *p=strchr(s,n);
		if(p){
			cout<<*(p-2);
		}
		else{
			cout<<n;
		}
	}
	return 0;
}
````
# 解題技巧:
使用反斜線要注意
````c++
//wrong answer
char s[]="1234567890-=qwertyuiop[]\asdfghjkl;'zxcvbnm,./";
//right answer
char s[]="1234567890-=qwertyuiop[]\\asdfghjkl;'zxcvbnm,./";
````
strchr(s,n)
s為查詢的字符串
n為要查找的字符，須為ASCII值
這題在對n做換小寫時就轉為ASCII
