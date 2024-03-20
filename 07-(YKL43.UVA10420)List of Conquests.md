# 題目: List of Conquests

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/4cd3d91c-0982-4c7b-8a82-e24597469b05)

# 程式碼
````C++
#include <iostream>
#include <map>
using namespace std;
int main(){
	int n;
	cin>>n;
	string country,fname,lname;
	map<string,int>cmap;
	while(cin>>country>>fname>>lname){
		cmap[country]++;
	}
	for(auto a:cmap){
		cout<<a.first<<" "<<a.second<<endl;
	}
}
````
# 解題技巧
用map(key value)
ex :
map  key   value
cmap first second

for(auto a:cmap)透過疊代的方式將容器內的元素取出賦予a值
