# Sort!Sort!!Sort!!!  
## 遇到問題:  
1. 使用while，修改程式碼後會注意到的參數問題
犯了一個很蠢的問題，原本想把程式全部寫在while裡面，後來又想改成調用函數，while導致參數值變小。
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
