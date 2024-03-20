# 題目:B2-Sequence
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/593be154-e442-4311-ab57-3f84cfa9dec4)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int N,b,count=0;
	while(cin>>N){
		count++;
		int a[N]={},sum[N*N]={};
		for(int i=0;i<N;i++){
			cin>>a[i];
		}
		bool isB2Sequence = true;
		for(int i=0;i<N;i++){
			for (int j=i;j<N;j++){
				int currentsum =a[i]+a[j];
				int index=currentsum;
				if(sum[index]==1){
					isB2Sequence=false;
					break;
				}
				else{
					sum[index]=1;
				}
			}
			if(!isB2Sequence){
				break;
			}
		}
		if(isB2Sequence){
            cout << "Case #" << count << ": It is a B2-Sequence." << endl<<endl;
        }
        else{
            cout << "Case #" << count << ": It is not a B2-Sequence." << endl<<endl;
        }
    }
	return 0;
}
````
# 解題技巧:
把總和加起來放進陣列內，重複就跳出迴圈
