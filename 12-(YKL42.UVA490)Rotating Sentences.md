#題目: Rotating Sentences

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/faefe372-6c85-4bd9-bee5-4f440fb669d5)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
    char a[1000][1000];
    string n;
    int row=0;
    int max=0;
    int maxpos=0;
    int length[500]={};
    while(getline(cin,n)){
        for(int i=0;i<n.size();i++){
            a[row][i]=n[i];
        }
        length[row]=n.size();
        if(n.size()>max){
            max=n.size();
            maxpos=row;
        }
        row++;
    }
    row--;
    for(int i=row;i>maxpos;i--){
        for(int j=length[i] ;j<max;j++){
            a[i][j] = ' ';
        }
    }
    int count=0;
    for(int i=0;i<max;i++){
            for(int j=row;j>=0;j--){
                if(count>row){
                    cout<<endl;
                    count=0;
                }
                cout<<a[j][i];
                count++;
            }
        }
    cout<<endl;
}
````
