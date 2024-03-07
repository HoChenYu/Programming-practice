#題目: Rotating Sentences

![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/faefe372-6c85-4bd9-bee5-4f440fb669d5)

#程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	char a[100][100];
	string n;
	int row;
	int max;
	
	while(getline(cin,n)){
		for(int i=0;i<n.size();i++){
			a[row][i]=n[i];
		}
		row++;
		if(n.size()>max){
			max=n.size();
		}
	}
	for (int i = n.size(); i < max; i++) {
            a[row][i] = ' ';
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
