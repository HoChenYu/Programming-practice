# 題目:Cheapest base
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/3299bc42-9be8-4e88-b824-6d5ef6892404)
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f7076a95-b6ac-430c-9e63-d5e4d191256c)
# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
    int x,number,n;
    cin>>x;
    int c;
    c=x;
    for(int t=1;t<=x;t++){
        cout<<"Case "<<t<<":"<<endl;
        int a[36]={};
        for(int i=0;i<36;i++){
            cin>>a[i];
        }
        cin>>n;
        while(n--){
        	int sum,cheaplist[36]={};
            cin>>number;
            int r,cheapest=	2147483647,copy,count=0;
            for(r=2;r<=36;r++){
                sum=0;
                copy=number;
                while(copy>0){
                    sum+=a[copy%r];
                    copy/=r;
                }
                if(sum<cheapest){
                	cheapest=sum;
                	cheaplist[0]=r;
                	count=1;
                }
                else if(sum==cheapest){
                	cheaplist[count++]=r;
                }
            }
            cout<<"Cheapest base(s) for number "<<number<<":";
            for(int i=0;i<count;i++){
            	cout<<" "<<cheaplist[i];
            }
            cout<<endl;
    	}
    	if(--c){
    		cout<<endl;
    	}
	}
}
````
# 解題技巧:
很多輸入(其中包含很多層迴圈),因此參數之間的copy比較容易混淆...，基本上這題應該就是暴力破解也沒別招
