### Diamond Pattern
```cpp
#include<bits/stdc++.h>
 using namespace std;
 int32_t main(){
     int n=5;
     for(int i=1;i<=n;i++){
         for(int j=1;j<=n-i;j++){
             cout<<"  ";
         }
         for(int j=1;j<=i;j++){
             cout<<"* ";
         }
         for(int j=2;j<=i;j++){
             cout<<"* ";
         }
         cout<<endl;
     }
     for(int i=n;i>=1;i--){
         for(int j=1;j<=n-i;j++){
             cout<<"  ";
         }
         for(int j=1;j<=i;j++){
             cout<<"* ";
         }
         for(int j=2;j<=i;j++){
             cout<<"* ";
         }
         cout<<endl;
     }
     return 0;
 }
```
### Palindromic Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout<<"  ";
        }
        for(int j=i;j>=1;j--){
            cout<<j<<" ";
        }
        for(int j=2;j<=i;j++){
            cout<<j<<" ";
        }   
        cout<<endl;
    }return 0;
}
```
### Number Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout<<" ";
        }
        for(int j=1;j<=i;j++){
            cout<<j<<" ";
        }
        cout<<endl;
    }return 0;
}
```
### Hollow Rhombus Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout<<"  ";
        }
        for(int j=1;j<=n;j++){
            if(i==1||j==1||i==n||j==n){
                cout<<"* ";
            }else{
                cout<<"  ";
            }
        }
        cout<<endl;
    }return 0;
}
```
### Rhombus Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout<<"  ";
        }
        for(int j=1;j<=i;j++){
            cout<<"* ";
        }
        for(int j=n-i;j>=1;j--){
            cout<<"* ";
        }
        cout<<endl;
    }return 0;
}
```
### Floyd's Triangle Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    int count=1;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            cout<<count<<" ";
            count++;
        }cout<<endl;
    }return 0;
}
```
### Half pyramid using after 180 degree rotaion
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout<<"  ";
        }
        for(int j=1;j<=i;j++){
            cout<<"* ";
        }cout<<endl;
    }return 0;
}
```
### Half Pyramid Using Numbers
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=n;i>=1;i--){
        for(int j=1;j<=i;j++){
            cout<<j<<" ";
        }cout<<endl;
    }return 0;
}
```
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
### Inverted Half Pyramid Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=n;i>=1;i--){
        for(int j=1;j<=i;j++){
            cout<<"* ";
        }cout<<endl;
    }return 0;
}
```
### Half Pyramid using numbers "0" & "1" Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            if((i+j)%2==0){
                cout<<1<<" ";
            }else{
                cout<<0<<" ";
            }
        }cout<<endl;
    }return 0;
}
```
