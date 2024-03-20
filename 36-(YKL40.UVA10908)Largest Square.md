# 題目:Largest Square
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/f27d8ee9-ef0d-45a6-ac86-47dbe0568bbd)
![image](https://github.com/HoChenYu/Programming-practice/assets/63805851/41d61daa-ca88-4b78-8019-38df96a7f669)

# 程式碼:
````C++
#include <iostream>
using namespace std;
int main(){
	int t,m,n,q,r,c;
	cin>>t;
	while(t--){
		cin>>m>>n>>q;
		char a[m][n];
		cout<<m<<" "<<n<<" "<<q<<endl;
		for (int i=0;i<m;i++){
			for(int j=0;j<n;j++){
				cin>>a[i][j];
			}
		}
		for (int i=0;i<q;i++){
			cin>>r>>c;
			char center;
			int radius=1;
			while(r-radius>=0 and r+radius<m and c-radius>=0 and c+radius<n){
				bool right=1;
				center=a[r][c];
				for(int j=r-radius;j<=r+radius;j++){
					for(int k=c-radius;k<=c+radius;k++){
						if(a[j][k]!=center){
							right=0;
							break;
						}
					}
					if(!right){
						break;
					}
				}
				if(!right){
					break;
				}
				radius++;					
			}
			cout<<2*(radius-1)+1<<endl;
		}
		
	}
}
````
# 幾題技巧:
在中心點往外擴張radius+1直到周圍有出現與center不同的char
