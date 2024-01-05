## 題目:Palindromes  
<img width="505" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/fe1b128c-d33a-4a9a-9ff9-c0a02bf4d9c0">  
<img width="520" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/f17d0368-7a39-4352-a26d-ed93c0ce0bcf">     
範例輸入和輸出：  
<img width="267" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/632f6d08-dd6f-4696-9788-171a00cd30bf">      
問題分析：  
存在兩個主要判斷，判斷的結果只有2種，所以最後會有4種結果。  
1. 是不是迴文 答案只有yes or no(所以這邊就會是使用回傳ture or false的 boolean函數)
2. 是不是鏡像 答案只有yes or no(所以一樣是boolean函數)  
## 流程圖:  
<img width="421" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/ffd4a5fa-0ae5-49c7-a23d-908264cafabd">

程式碼:  
````C++
#include <iostream>
#include <string>
#include <unordered_map>
using namespace std;
bool palidrome(string s){
	for(int i=0;i<s.length()/2;i++){
		if(s[i]!=s[s.length()-1-i]){
			return false;
		}
	}
	return true;
}
bool mirrored(string s){
	unordered_map<char, char> mirrorMap = {
        {'A', 'A'}, {'E', '3'}, {'H', 'H'}, {'I', 'I'}, {'J', 'L'},
        {'L', 'J'}, {'M', 'M'}, {'O', 'O'}, {'S', '2'}, {'T', 'T'},
        {'U', 'U'}, {'V', 'V'}, {'W', 'W'}, {'X', 'X'}, {'Y', 'Y'}, {'Z', '5'},
        {'1', '1'}, {'2', 'S'}, {'3', 'E'}, {'5', 'Z'}, {'8', '8'}
    };
	bool a=true;
	for(int i=0;i<s.length()/2;i++){
		char current =s[i];
		char mirror = s[s.length()-1-i];
		if(mirrorMap.find(current) != mirrorMap.end() && mirrorMap[current] == mirror){
            continue;
        } else {
            a = false;
            break;
        }
    }
	return a;
}
int main(){
	string str1;
	int len;
	while(cin>>str1){
		if(palidrome(str1)){
			if(mirrored(str1)){
				cout<<str1<<" -- is a mirrored palindrome."<<endl<<endl;
			}
			else{
				cout<<str1<<" -- is a regular palindrome."<<endl<<endl; 
			}
		}
		else{
			if(mirrored(str1)){
				cout<<str1<<" -- is a mirrored string."<<endl<<endl;
			}
			else{
				cout<<str1<<" -- is not a palindrome."<<endl<<endl;
			}
		}
	}

}

````
