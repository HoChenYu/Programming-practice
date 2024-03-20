# 題目:Common Permutation
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/bdd54e45-6fc7-4057-9e39-348a17697f40)

# 程式碼:
````C++
#include <iostream>
#include <algorithm>
using namespace std;
string equal(string a,string b){
	string c;
	sort(a.begin(),a.end());
	sort(b.begin(),b.end());
	for(int i=0, j=0; i<a.size() && j<b.size();){
		if(a[i]==b[j]&& a[i]!=' '){
			c+=a[i];
			i++;
			j++;
		}else if (a[i] <b[j]){
			i++;
		}else{
			j++;
		}
	}

    return c;
}
int main(){
	string letter1,letter2;
	while(getline(cin, letter1)){
			getline(cin,letter2);
			cout<<equal(letter1,letter2)<<endl;	
		}
	}
````
# 解題技巧:

這題很煩的是測資，要處理字串中夾著空白和兩個字串都是空白的情況，所以只能使用getline或get一個一個處理  

一開始先用sort排序兩個不同的字串，因為排序過了，所以只需要讓當前string中比較小的char做++追趕上另一個string，ex(以排序完畢):string1:aacccddee;string2:cdddeee;string1要一直++到c直到與string2匹配
