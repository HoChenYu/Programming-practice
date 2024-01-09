# Sort!Sort!!Sort!!!  
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
