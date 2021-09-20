### Linear Search
```cpp
#include<bits/stdc++.h>
using namespace std;

int linearSearch(int array[], int n, int key){
    for(int i=0;i<n;i++){
        if(array[i]==key){
            return i;
        }
    }
    return -1;
}

int32_t main(){
    int n;
    cin>>n;
    int array[n];
    for(int i=0;i<n;i++){
        cin>>array[i];
    }
    int key;
    cin>>key;
    cout<<linearSearch(array,n,key)<<endl;
    
    return 0;
}
```
### Binary Search
```cpp
#include<bits/stdc++.h>
using namespace std;

int binarySearch(int array[],int n,int key){
    int start = 0;
    int end=n;

    while(start<=end){
        int mid=(start+end)/2;

        if(array[mid]==key){
            return mid;
        }
        else if(array[mid]>key){
            end=mid-1;
        }else{
            start=mid+1;
        }
    }
    return -1;
}

int32_t main(){
    int n;
    cin>>n;
    int array[n];
    for(int i=0;i<n;i++){
        cin>>array[i];
    }
    int key;
    cin>>key;
    cout<<binarySearch(array,n,key);
    return 0;
}
```
### Program to declare array
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int Marvel_mem[5]={5,6,7,4,3};
    cout<<Marvel_mem[0];
}
```
### Program to take take input from user and then make array
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int size;
    cout<<"eneter the size of the array"<<endl;
    cin>>size;
    int array[size];
    for(int i=0; i<size; i++){
        cin>>array[i];
        cout<<array[i];
    }
    for(int i=0; i<size; i++){  // another way
        cout<<array[i]<<" ";
    }
}
```
### Program to take input of an array of size n and then find maximum and minimum values
```cpp
#include<bits/stdc++.h>
using namespace std;
int32_t main(){
    int n;
    cin>>n;
    int array[n];
    for(int i=0; i<n; i++){
        cin>>array[i];
    }
    int maximum=INT32_MIN;
    int minimum=INT32_MAX;

    for(int i=0; i<n; i++){
        maximum=max(maximum,array[i]);
        minimum=min(minimum,array[i]);
    }
    cout<<"Max no.="<<maximum<<endl;
    cout<<"Min no.="<<minimum<<endl;
}
```
### Program to print Kids With the Greatest Number of Candies
```cpp
#include<bits/stdc++.h>
using namespace std;



int32_t main(){
    int n,i;
    cin>>n;
    int array[n];
    for(i=0; i<n; i++){
        cin>>array[i];
    }
    int extracandidate;
    cin>>extracandidate;

    int maximum=INT32_MIN;
    
    for(i=0; i<n; i++){
        maximum=max(maximum,array[i]);
    }
    
    for(i=0; i<n; i++){
        if(array[i]+extracandidate>=maximum){
            cout<<"true"<<endl;
        }else{
            cout<<"false"<<endl;
        }
    }
    return 0;
}
```
### Program to print Running Sum of 1d Array
```cpp
#include <bits/stdc++.h>
using namespace std;
 
// Driver code
int main()
{
    int n;
    cin>>n;
    int array[n];
    int sum=0;
    for(int i=0; i<n; i++){
        cin>>array[i];
        sum+=array[i];
        cout<<sum<<endl;
    }
    return 0;
}
```
### Add two binary numbers
```cpp
#include<bits/stdc++.h>
using namespace std;

int reverse(int num){
    int new_num=0;
    while(num>0){
        int lastdigit=num%10;
        new_num=new_num*10+lastdigit;
        num/=10;
    }
    return new_num;
}

int addBinary(int a,int b){
    int new_num=0;
    int previous_carry=0;
    while(a>0 &&b>0){
        if(a%2==0 && b%2==0){
            new_num=new_num*10+previous_carry;
            previous_carry=0;
        }
        else if((a%2==0 && b%2==1) || (a%2==1 && b%2==0)){
            if(previous_carry==1){
                new_num=new_num*10+0;
                previous_carry=1;
            }
            else{
                new_num=new_num*10+1;
                previous_carry=0;
            }
        }
        else{
            new_num=new_num*10+previous_carry;
            previous_carry=1;
        }
        a/=10;
        b/=10;
    }

    while(a>0){
        if(previous_carry==1){
            if(a%2==1){
                new_num=new_num*10+0;
                previous_carry=1;
            }
            else{
                new_num=new_num*10+1;
                previous_carry=0;
            }
        }
        else{
            new_num=new_num*10+(a%10);
        }
        a/=10;
    }

    while(b>0){
        if(previous_carry==1){
            if(b%2==1){
                new_num=new_num*10+0;
                previous_carry=1;
            }
            else{
                new_num=new_num*10+1;
                previous_carry=0;
            }
        }
        else{
            new_num=new_num*10+(b%10);
        }
        b/=10;
    }
    if(previous_carry==1){
        new_num=new_num*10+1;
    }
    new_num=reverse(new_num);
    return new_num;
}


int32_t main(){
    int a,b;
    cin>>a>>b;
    cout<<addBinary(a,b);
    return 0;
}
```
### Sum of n natural numbers
```cpp
#include<bits/stdc++.h>
using namespace std;

int sumOfNums(int n) {
    int sum;
    sum=(n*(n+1))/2;
    return sum;
}

int32_t main(){
    int num;
    cin>>num;
    cout<<sumOfNums(num);
    return 0;
}
```
### Check whether the given triplet is pyhagorian triplet or not
```cpp
#include<bits/stdc++.h>
using namespace std;

int maximumNumber(int a, int b, int c){
    int max;
    if(a>b&&a>c){
        max=a;
    }if(b>a&&b>c){
        max=b;
    }if(c>a&&c>b){
        max=c;
    }
    return max;
}

bool check(int a, int b,int c){
    int x= max(a,max(b,c));// max function is inbuilt function which can find maximum among two numbers
    //int x= maximumNumber(a,b,c); You can also use this function to call above one 
    int y,z;
    if(x==a){
        y=b;
        z=c;
    }else if(x==b){
        y=a;
        z=c;
    }else{
        y=b;
        z=a;
    }
    if(pow(x,2)==pow(y,2)+pow(z,2)){
        return true;
    }else{
        return false;
    }
}

int main(){
    int a,b,c;
    cin>>a>>b>>c;
    if(check(a,b,c)){
        cout<<"Pythagorian triplet"<<endl;
    }else{
        cout<<"Not pythagorian triplet"<<endl;
    }
    return 0;
}
```
### Octal number to decimal number
```cpp
#include<bits/stdc++.h>
using namespace std;

int OctalToBinary(int num){
    int new_num=0;
    int count=0;
    while(num>0){
        int remainder = num%10;
        new_num = (remainder*pow(8,count))+new_num;
        num/=10;
        count++;
    }
    return new_num;
}

int32_t main(){
    int n;
    cin>>n;
    cout<<OctalToBinary(n);
    return 0;
}
```
### Decimal to octal representation
```cpp
#include<bits/stdc++.h>
using namespace std;

int DecimalToOctal(int num){
    int new_num=0;
    int count=1;
    while(count<=num){
        count*=8;
    }count/=8;

    while(count>0){
        int lastdigit=num/count;
        num=num-lastdigit*count;
        count/=8;
        new_num=(new_num*10)+lastdigit;
    }
    return new_num;
}

int32_t main(){
    int n;
    cin>>n;
    cout<<DecimalToOctal(n);
    return 0;
}
```
### Hexadecimal to decimal representation
```cpp
#include<bits/stdc++.h>
using namespace std;

int HexaDecimaltoDecimal(string str){
    int new_num = 0;
    int count = 1;
    int s=str.size();
    for(int i=s-1;i>=0;i--){
        if(str[i]>='0' && str[i]<='9'){
            new_num=new_num+count*(str[i]-'0');
        }else if(str[i]>='A' && str[i]<='F'){
            new_num=new_num+count*(str[i]-'A'+10);
        }
        count*=16;
    }
    return new_num;
}

int32_t main(){
    string n;
    cin>>n;
    cout<<HexaDecimaltoDecimal(n)<<endl;
    return 0;
}
```
### Decimal to Hexadecimal representation
```cpp
#include<bits/stdc++.h>
using namespace std;

string DecimaltoHex(int str){
    string new_num="";
    int count=1;
    while(count<=str){
        count*=16;
    }count/=16;

    while(count>0){
        int lastdigit=str/count;
        str=str-lastdigit*count;
        count/=16;
        if(lastdigit<=9){
            new_num=new_num + to_string(lastdigit);
        }else{
            char c ='A'+lastdigit-10;
            new_num.push_back(c);
        }
    }
    return new_num;
}

int32_t main(){
    int n;
    cin>>n;
    cout<<DecimaltoHex(n)<<endl;
    return 0;
}
```
### Program using functions to check if a person is eligible for voting or not by comparing his age with legal voting age i.e. 18
```cpp
#include<bits/stdc++.h>
using namespace std;

bool checkVotingAge(int age) {
    if(age>=18){
        return true;
    }
    return false;
}

int32_t main(){
    int age;
    cin>>age;
    if(checkVotingAge(age)){
        cout<<"Eligible voter"<<endl;
    }else{
        cout<<"Not eligible voter";
    }
    return 0;
}
```
###  Program with a function to swap the values of 2 given integer variables
```cpp
#include<bits/stdc++.h>
using namespace std;

int32_t main(){
    int a,b;
    cin>>a>>b;
    swap(a,b);
    cout<<"a="<<a<<endl;
    cout<<"b="<<b<<endl;
    return 0;
}
```
###  Program with two functions to print the maximum and the minimum number respectively among three numbers entered by user
```cpp
#include<bits/stdc++.h>
using namespace std;

int maximumNumber(int a, int b, int c){
    int max;
    if(a>b&&a>c){
        max=a;
    }if(b>a&&b>c){
        max=b;
    }if(c>a&&c>b){
        max=c;
    }
    return max;
}

int minimumNumber(int a, int b, int c){
    int min;
    if(a<b&&a<c){
        min=a;
    }if(b<a&&b<c){
        min=b;
    }if(c<a&&c<b){
        min=c;
    }
    return min;
}

int32_t main() {
    int n1,n2,n3;
    cin >> n1 >> n2 >> n3;
    cout<<"Max="<<maximumNumber(n1,n2,n3)<<endl;
    cout<<"Min="<<minimumNumber(n1,n2,n3);
    return 0;
}
```
###  Program to find out whether a given character is an alphabet or not using functions
```cpp
#include<bits/stdc++.h>
using namespace std;

bool isAlphabet(char c){
    if((c>=97&&c<=122) || (c>=65&&c<=90)){
        return true;
    }
    return false;
}

int32_t main(){
    char ch;
    cin>>ch;
    if(isAlphabet(ch)){
        cout<<"Alphabet";
    }else{
        cout<<"Try Something else...";
    }
    return 0;
}
```
###  Program to find out whether a given number is even or odd using functions
```cpp
#include<bits/stdc++.h>
using namespace std;

bool isEvenorOdd(int num){
    if(num%2==0){
        return false;
    }
    return true;
}

int32_t main(){
    int n;
    cin>>n;
    if(isEvenorOdd(n)){
        cout<<"Odd";
    }else{
        cout<<"Even";
    }
    return 0;
}
```
### Program to Print Pascal Triangle
```cpp
#include <bits/stdc++.h>
using namespace std;

int fact(int num){
    int factorial=1;
    for(int i=1;i<=num;i++){
        factorial=factorial*i;
    }
    return factorial;
}

int32_t main(){
    int num;
    cin>>num;
    for(int i=0;i<num;i++){
        for(int j=0;j<=i;j++){
            int Position=(fact(i)/(fact(i-j)*fact(j)));
            cout<<Position<<" ";
        }cout<<endl;        
    }
    return 0;
}
```
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
