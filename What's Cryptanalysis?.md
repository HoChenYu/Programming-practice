# 題目:What's Cryptanalysis?

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/88ff6818-6153-4631-b818-605bd5274ce7)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int x[256],len;
int main(){
	char n;
	while(cin>>n){
		x[toupper(n)]++;
		len++;
	}
	while(--len){
		for(n='A';n<='Z';n++){
			if(len==x[n])
			{
				cout<<n<<" "<<x[n]<<endl;
			}
		}
	}
}
````
# 解題要點
 toupper(n) 將字符轉為大寫的ASCII值
 --len 因為開頭輸入的數字ex:3 不重要且會進入到while使得 len++
