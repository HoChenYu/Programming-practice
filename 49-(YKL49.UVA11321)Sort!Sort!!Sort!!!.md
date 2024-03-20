# 題目:Sort!Sort!!Sort!!!  
<img width="638" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/b53900fa-e18f-40b1-82bb-5e83af1d34ca">

## 範例輸入和輸出:
<img width="108" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/9d45ece7-0240-4156-b5b3-3151f322a52d">
<img width="102" alt="image" src="https://github.com/HoChenYu/Programming-practice/assets/63805851/31af1833-e9db-440d-b0cd-af4146d20bcc">  

## 問題分析:
題目為什麼叫sort!sort!!sort!!!，就是要進行三次的sorting，第一次是mod後的結果從小排到大，二、三次是遇到奇數和偶數的排序方式不同，偶數是小到大，奇數是大到小。
## 程式碼:
````C++
#include <iostream>
using namespace std;
void modsorting(int n,int a[],int m){
    //mod排序 從小到大
    int tmp1,tmp2,tmp3;
    for(int i=0;i<n;i++){
        for(int j=0;j<n-1-i;j++){
        if(a[j]%m>a[j+1]%m)
        {
            tmp1=a[j+1];
            a[j+1]=a[j];
            a[j]=tmp1;
        }
        else if(a[j]%m==a[j+1]%m){
            if(a[j]%2==1){
                if(a[j]<a[j+1]){
                    tmp2=a[j];
                    a[j]=a[j+1];
                    a[j+1]=tmp2;
                }
            }
            else if(a[j]%2==0){
                if(a[j]>a[j+1]){
                    tmp3=a[j+1];
                    a[j+1]=a[j];
                    a[j]=tmp3;
                }
            }
        }
        }
    }
}
int main(){
    int N,M;
    cin>>N>>M;
    int array[N];
    for (int i = 0; i < N; i++) {
        cin >> array[i];
    }
    modsorting(N,array,M);
    cout<<N<<" "<<M<<endl;
    for(int i=0;i<N;i++){
        cout<< array[i] <<endl;
    }
    cout<<"0 0"<<endl;

} 
````
## 遇到問題:  
### 1. 使用while，修改程式碼後會注意到的參數問題  
犯了一個很蠢的問題，原本想把程式全部寫在while裡面，後來又想改成調用函數，while導致參數值N變小。
````C++
int main(){
    int N,M;
    cin>>N>>M;
    int array[N];
    while(N){
        //從後面開始放直到array[0]
        cin>>array[N-1];
        N--;
    }
    modsorting(N,array[N],M)
    for(int i=0;i<N;i++){
    	cout<< array[i] <<endl;
    }
}
````
時時刻刻提醒自己在使用while函數上要特別注意。
