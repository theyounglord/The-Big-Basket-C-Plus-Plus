### Rectangle Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int rows,cols;
    cin>>rows>>cols;
    for(int i=1;i<=rows;i++){
        for(int j=1;j<=cols;j++){
            cout<<"* ";
        }cout<<endl;
    }
    return 0;
}
```
### Hollow Rectangle Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int rows,cols;
    cin>>rows>>cols;
    for(int i=1;i<=rows;i++){
        for(int j=1;j<=cols;j++){
            if(i==1||i==rows||j==1||j==cols){
                cout<<"* ";
            }else{
                cout<<"  ";
            }
        }cout<<endl;
    }
    return 0;
}
```
### Half Pyramid Using Numbers Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            cout<<i<<" ";
        }cout<<endl;
    }return 0;
}
```
