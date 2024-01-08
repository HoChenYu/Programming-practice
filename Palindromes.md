# 題目:Palindromes  
<img width="505" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/fe1b128c-d33a-4a9a-9ff9-c0a02bf4d9c0">  
<img width="520" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/f17d0368-7a39-4352-a26d-ed93c0ce0bcf">  
  
## 範例輸入和輸出：  
<img width="267" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/632f6d08-dd6f-4696-9788-171a00cd30bf">  

## 問題分析：  
存在兩個主要判斷，判斷的結果只有2種，所以最後會有4種結果。  
1. 是不是迴文 答案只有yes or no(所以這邊就會是使用回傳ture or false的 boolean函數)
2. 是不是鏡像 答案只有yes or no(所以一樣是boolean函數)

## 流程圖:  
<img width="421" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/ffd4a5fa-0ae5-49c7-a23d-908264cafabd">

## 程式碼:  
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

## 遇到問題:  
1. 邏輯錯誤
````C++
bool palidrome(string s){
	bool a=true;
	for(int i=0;i<s.length()/2;i++){
		if(s[i]==s[s.length()-1-i]){a=true;}
		else{a=false;}
	}
	return a;
}
````
預設返回a值，上述程式碼並未在發現錯誤時就停止，而是繼續檢查，變成說檢查到最靠近中間那項(也就是最後一次檢查)，只要他是true就會返回true，這樣的方式是錯誤的，ex:abcde，a和e是false，但b和d是true且為最後檢查，返回true。
應該改為一遇到不相符的結果立即返回
````C++
bool palidrome(string s){
	bool a=true;
	for(int i=0;i<s.length()/2;i++){
		if(s[i]!=s[s.length()-1-i]){a=false;}
	}
	return a;
}
````
## 學習新知:
### unordered_map  

就是常見的key value，且為未排序，時間複雜度O(1)  

建立一個為<char,char>的表:  

````C++
unordered_map<char, char> mirrorMap = {
        {'A', 'A'}, {'E', '3'}, {'H', 'H'}, {'I', 'I'}, {'J', 'L'},
        {'L', 'J'}, {'M', 'M'}, {'O', 'O'}, {'S', '2'}, {'T', 'T'},
        {'U', 'U'}, {'V', 'V'}, {'W', 'W'}, {'X', 'X'}, {'Y', 'Y'}, {'Z', '5'},
        {'1', '1'}, {'2', 'S'}, {'3', 'E'}, {'5', 'Z'}, {'8', '8'}
    };
````

主要判斷式:  

````C++
if(mirrorMap.find(current) != mirrorMap.end() && mirrorMap[current] == mirror)
````
意思就是透過find()函式找current這個參數是否在表上搜索的到，若無則會回傳.end()這個函式，若有則回傳他在第幾個ex:second。所以是透過不等於的判斷式找到表上有對應的key，並且找到對應的value。  

2024/1/5寫完該題 2024/1/8補充說明
