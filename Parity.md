# 題目:Parity
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/0e47b62b-f351-45e4-a1f6-98be0f7dc6d2)

# 程式碼:
````C++
#include <iostream>
#include <stack>
using namespace std;
stack<int>n;
int main(){
	long long I;
	while(cin>>I,I){
		int last=0;
		while(I){
			last+=I%2;
			n.push(I%2);
			I/=2;
		}
		cout<<"The parity of ";
		while(n.size()){
			cout<<n.top();
			n.pop();
		}
		cout<<" is "<<last<<" (mod 2)."<<endl;
	}
	
}
````

# 解題技巧
這邊用到資料結構的stack，透過mod2取最後一個bit的結果last，將last push到stack內，stack的規則是先進後出，top是stack最上面的元素，看一下top然後pop掉直到stack.size()==0
