### Program to calculate nCr i.e Binary coefficient using functions
```cpp
#include<bits/stdc++.h>
using namespace std;

int fact(int num){
    int factorial=1;
    for(int i=1;i<=num;i++){
        factorial=factorial*i;
    }
    return factorial;
}

int32_t main(){
    int n;
    cin>>n;
    int answer = fact(n);
    cout<<answer<<endl;
    return 0;
}
```
### Program to find a fibonaci sequence till n
```cpp
#include <bits/stdc++.h>
using namespace std;

void fib(int num){
    int n1=0;
    int n2=1;
    int next_num;
    for(int i=1;i<=num;i++){
        cout<<n1<<endl;
        next_num=n1+n2;
        n1=n2;
        n2=next_num;
    }
    return;
}

int32_t main(){
    int n;
    cin>>n;
    fib(n);
    return 0;
}
```
### Check prime or not using function
```cpp
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int num){
    for(int i=2;i<=sqrt(num);i++){
        if(num%i==0){
            return false;
        }
    }
    return true;
}
int32_t main() {
    int n;
    cout<<"enter your number"<<endl;
    cin>>n;
    if(isPrime(n)){
        cout<<"Prime";
    }else{
        cout<<"Non Prime";
    }
}
```
### Print Prime betwwen a range of number
```cpp
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int num){
    for(int i=2;i<=sqrt(num);i++){
        if(num%i==0){
            return false;
        }
    }
    return true;
}

int32_t main() {
    int a,b;
    cin>>a>>b;
    for(int i=a;i<=b;i++){
        if(isPrime(i)){
            cout<<i<<endl;
        }else{
            continue;
        }
    }
    return 0;
}
```
### program to add 2 numbers using functions
```cpp
#include<bits/stdc++.h>
using namespace std;

int add(int n1,int n2){
    int sum=n1+n2;
    return sum;
}

int32_t main(){
    int a,b;
    cin>>a>>b;
    cout<<add(a,b)<<endl;
    return 0;
}
```
### program to print a given number using functions
```cpp
#include<bits/stdc++.h>
using namespace std;

void display(int num){
    cout<<"Your num="<<num<<endl;
    return ;
}
int32_t main(){
    int a;
    cin>>a;
    display(a);
    return 0;
}
```
### program to print the factorial of two numbers using functioms
```cpp
#include<bits/stdc++.h>
using namespace std;

int factorial(int num){
    int fact=1;
    for(int i=num;i>=1;i--){
        fact=fact*i;
    }
    return fact;
}

int32_t main(){
    int n1,n2;
    cin>>n;
    cout<<"Factorial of "<<n1<<"="<<factorial(n1);
    cout<<"Factorial of "<<n2<<"="<<factorial(n2);
    return 0;
}
```
### Factorial
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n;
    cin>>n;
    int fact=1;
    for(int i=1;i<=n;i++){
        fact=fact*i;
    }
    cout<<fact;
    return 0;
}
```
### Binary to Decimal
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n;
    cout<<"Enter Only Binary number to convert it into Decimal"<<endl;
    cin>>n;
    int count=0;
    int sum=0;
    while(n>0){
        int lastdigit=n%10;
        sum+=pow(2,count)*lastdigit;
        n=n/10;
        count++;
    }
    cout<<sum<<endl;
    return 0;
}
```
### Revese a number
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n;
    cin>>n;
    int reverse=0;
    while (n>0)
    {
        int lastdigit=n%10;
        reverse=reverse*10 + lastdigit;
        n=n/10;
    }
    cout<<reverse<<endl;
    return 0;
}
```
### Armstrong or not
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n;
    cin>>n;
    int original_num=n;
    // code to check the length of number
    int count=0;
    while (original_num>0){
        original_num=original_num/10;
        count++;
    }
    original_num=n; // Origianl number is reassigned to n
    
    int sum=0;
    while(n>0){
        int lastdigit=n%10;
        sum+=(pow(lastdigit,count));
        n=n/10;
    }
    if(sum==original_num){
        cout<<"Armstrong";
    }else{
        cout<<"Not an armstrong";
    }
    return 0;
}
```
### Zig Zag Pattern
```cpp
#include<bits/stdc++.h>
 using namespace std;
 int32_t main(){
     int n=9;
     for(int i=1;i<=3;i++){
         for(int j=1;j<=n;j++){
             if((i+j)%4==0||i==2&&(i+j)%2==0){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }cout<<endl;
     }return 0;
 }
```
### Hollow Butter-Fly Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            if(j==1||j==i){
                cout<<"*";
            }else{
                cout<<" ";
            }
        }
        for(int j=1;j<=2*n-2*i;j++){
            cout<<" ";
        }
        for(int j=1;j<=i;j++){
            if(j==1||j==i){
                cout<<"*";
            }else{
                cout<<" ";
            }
        }
        cout<<endl;
    }
    for(int i=n;i>=1;i--){
        for(int j=1;j<=i;j++){
            if(j==1||j==i){
                cout<<"*";
            }else{
                cout<<" ";
            }
        }
        for(int j=1;j<=2*n-2*i;j++){
            cout<<" ";
        }
        for(int j=1;j<=i;j++){
            if(j==1||j==i){
                cout<<"*";
            }else{
                cout<<" ";
            }
        }
        cout<<endl;
    }
    return 0;
}
```
### Butter-Fly Pattern
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n=5;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            cout<<"*";
        }
        for(int j=1;j<=2*n-2*i;j++){
            cout<<" ";
        }
        for(int j=1;j<=i;j++){
            cout<<"*";
        }
        cout<<endl;
    }
    for(int i=n;i>=1;i--){
        for(int j=1;j<=i;j++){
            cout<<"*";
        }
        for(int j=1;j<=2*n-2*i;j++){
            cout<<" ";
        }
        for(int j=1;j<=i;j++){
            cout<<"*";
        }
        cout<<endl;
    }
    return 0;
}
```
### Hollow Diamond Pattern inscribed in rectangle
```cpp
#include<bits/stdc++.h>
 using namespace std;
 int32_t main(){
     int n=5;
     for(int i=1;i<=n;i++){
         for(int j=1;j<=n-i;j++){
             cout<<"* ";
         }
         for(int j=1;j<=i;j++){
             if(j==1){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         for(int j=2;j<=i;j++){
             if(j==i){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         for(int j=n-i;j>=1;j--){
             cout<<"* ";
         }
         cout<<endl;
     }
     for(int i=n;i>=1;i--){
         for(int j=1;j<=n-i;j++){
             cout<<"* ";
         }
         for(int j=1;j<=i;j++){
             if(j==1){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         for(int j=2;j<=i;j++){
             if(j==i){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         for(int j=n-i;j>=1;j--){
             cout<<"* ";
         }
         cout<<endl;
     }
     return 0;
 }
```
### Hollow Diamond Pattern
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
             if(j==1){
                 cout<<"* ";`
             }else{
                 cout<<"  ";
             }
         }
         for(int j=2;j<=i;j++){
             if(j==i){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         cout<<endl;
     }
     for(int i=n;i>=1;i--){
         for(int j=1;j<=n-i;j++){
             cout<<"  ";
         }
         for(int j=1;j<=i;j++){
             if(j==1){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         for(int j=2;j<=i;j++){
             if(j==i){
                 cout<<"* ";
             }else{
                 cout<<"  ";
             }
         }
         cout<<endl;
     }
     return 0;
 }
```
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
