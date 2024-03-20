# 題目:Hardwood species
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/aa41a560-029a-4d74-98dd-6d130f56340c)
# 範例input&output
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/23a21d0d-814b-4b65-ad1c-4c9cd9a59a13)![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/019b8a73-92fb-4df8-9827-ba97e9f9dfcf)
# 程式碼:
````C++
#include <iostream>
#include <map>
#include <iomanip>
using namespace std;
int main(){
	int n;
	cin>>n;
	char c;
	c=getchar();
	c=getchar();
	while(n--){
		double sum=0;
		string s;
		map <string,double>Hardwoods;
		while(getline(cin,s)){
			if(s==""){
			break;
			}
			Hardwoods[s]++;
			sum++;
		}
		for(auto i:Hardwoods){
			cout<<fixed<<setprecision(4)<<i.first<<" "<<i.second/sum*100<<endl;
		}

		if(n){
		cout<<endl;
		}
	}
	return 0;
}
````
# 解題技巧:
用C++中的key value去計算key出現的次數，這題要注意因為cin>>1之後cache還會留存換行符號，所以要getchar()兩次或是getline(cin,n)兩次
