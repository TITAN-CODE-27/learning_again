# Exit control loop
## do while loop

```c
// syntax
do{
    statement;
    inc/dec;
}while(condition);  // compulsion ;
```
```c
 int i = 1;
 do{
    printf("%d" , i);
    i++
 }whie(i <= 5);
//  outputs : 1 , 2 , 3 , 4 , 5
```
### 32 Total numbers of keywords

### left shift operator
```c
//  left shift operator doubles
10 = 5 << 1
14 = 7 << 1
20 = 5 << 2
```

### right shift operator
```c
2 = 5 >> 1
3 = 7 >> 1
```

# Difference between C and C++
| C          | C++                       |
|------------|---------------------------|
|#include<stdio.h> | #include std \<iostream> |
|includes printf scanf | std librarary has iostream and has cin cout endl |
| printf("%d ", a); | cout << a ; |
|                   | cout is object of class ostream |
|                   | << is insertion operator        |
| scanf("%d",&a)    | cin >> a; |
|                   | cin is object of class istream | 
|                   |  |


```cpp
#include <iostream>
int main(){
    std::cout << 5 << 1 << std::endl; // 51
    std::cout <<(5<<1)<<std::endl;  //10
    return 0;
}
```

### what is namespace
```cpp
#include <iostream>
using namespace std;
namespace p1{
    int a = 5;
}
namespace p2{
    float a = 5.4f;
}

int main(){
    cout << p1::a <<endl;
    cout << p2::a <<endl;
    return 0;
}
```

```c
#include <iostream>
namespace INDIA{
    class hello{
        public:
        void print(){
            std::cout << "hello maya";
        }
    };
}
using namespace INDIA;
int main()
{
    hello h;
    h.print();
    return 0;
}
```

### MANIPULATOR
` std::endl  referes to end Of Line which is a manipulator`

` :: scope resolution operator`

## Variables
`Local Variables are initialized by garbage value`

`Global Varibales are initialized by 0`

```cpp
int b = 10; // global variable
int main(){
    int a = 5;  //local variable
    cout << a;
    cout << b;
}
```

####  if local and global variable have same variable weightage to local will be given
```cpp
int a = 5;
int main(){
    int a = 10;
    std::cout << a; // prints 10;
    std::cout << a; // prints 5;
}
```
`use scope resolutio :: operator to print the global variables when local is of same name ` 

## sum of two numbers

```cpp
#include <iostream>
using namespace std;
int main(){
    int a , b , sum ;
    cout <<'enter two numbers: ';
    // cerr <<"Error message "  For printing error message
    cin >> a >> b;
    sum = a + b;
    cout << sum;
    return 0;
}
```

`std::cout<< oct << number` for printing in octal

`std::cout<< hex << number` for printing in hex 

`cerr refers to console error `


# Import all header files
```cpp
#include <bits/stdc++.h>
// this header file includes all header files
```

# Function
### Types of functions
- Predefined function
  - header file import
  - call
- User Defined function
  - define it
  - call

```c
        int max(int , int)
        |         |______|__
        |                   |
    //return type           parameter / argument / input
```

```cpp
#include <bits/stdc++.h>
int maxx(int a , int b){
    return a > b ? a : b;
}
int main(){
    int a = 4 , b = 10;
    std::cout <<"Max is: "<< maxx(a,b); 
    return 0;
}
```

std::cout <<"Max is: "<<` maxx(a,b); ` Here maxx(a,b) is `actual parameter`

int `maxx(int a , int b)` Here int a , int b are `formal parameter` 

- Q1 sum of two numbers
    ```cpp
    int sum(int a , int b){
        return a+b;
    }

    int main(){
        int a = 5, b =10;
        cout << sum(a,b);
        return 0;
    }
    ```
- Q2 average of two numbers
    ```cpp
    int avg(int a , int b){
        return (a+b)/2;
    }
    
    int main(){
        int a = 5, b =10;
        cout << avg(a,b);
        return 0;
    }
    ```

## Function must be declared before calling
declare()

use()
```cpp
define(){<-----------
                    |
}                   |
main(){             |
    call();         |
}                   Bottom up approach
```

```cpp
                 
main(){             
    call(); ---------        
}                   |
                    |
define(){<----------|   Top down approach
                    
}                
```

## NOTE: A function can accept any number of arguments but can return maximum one output

what will happen

```cpp
int square (int x , int y , int z ){
    return x*x , y*y , z*z;
}
int main(){
    cout << square(5,6,7);
    return 0;
}
// outputs 49  as , operator will check from left to right but it will return the rightmost element
```

## NOTE: If a function does not return any value then it is called as VOID Function.


VOID FUNCTION
```cpp
void square (int x , int y , int z ){
    std::cout << x*x << y*y << z*z;
}
int main(){
    square(5,6,7);
    return 0;
}
// outputs 49  as , operator will check from left to right but it will return the rightmost element
```


# Call by Value

```cpp
// as the parameter is not a reference it updates only the copy
void increment(int a){
    a++;
}
int main(){
    int a = 5;
    increment(a);
    cout<< a;   // a prints 5
    return 0;
}
```

```cpp
// as the parameter is not a reference it updates only the copy
int increment(int a){
    a++;
    return a;
}
int main(){
    int a = 5;
    a = increment(a);
    cout<< a;   // a prints 6
    return 0;
}
```

## Function drawback
- slow execution speed 
  - SOLUTION: we can use `macro` function   

# Normal function
```cpp
int sum (int x , int y){
    return x+y;
}
int main(){
    cout << sum(5,6);
    cout << sum(5,8);
    return 0
}
```
# Macro Function
```cpp
                    //code
# define sum(a+b)    (a+b)
//        macro func
int main(){
    cout << sum(5,6);
    return 0;
}
```
cout << ~~sum(5,6)~~ << (5+7);

## NOTE: In c++ no need to use macro function only add INLINE keyword befor the function definition

## Inline function
```cpp
inline int sum (int x , int y){
    return x+y;
}
int main(){
    cout << sum(5,6);
    cout << sum(5,8);
    return 0
}
```



### used for multiline value
```c
for multiple line 
printf("               \
                       \
                       \
                       ");
```

# FUNCTION OVERLOADING (in C++)
when two or more functions having same name but different arguments then it is called as function overloading.
It is also called as `POLYMORPHISM` 

```cpp
#include <iostream>
int sum(int a , int b){
    return a + b;
}
float sum(float a , float b){
    return a + b;
}
int main(){
    std::cout << sum(5.4f, 6.4f) << std::endl;
    std::cout << sum(5, 6);
    return 0;
}       // output is 11.8 11
```

### Problem 
- same code is being repeated many times

Solution
# Template
```cpp
#include <iostream>

template<class T>
T sum (T x , T y){
    T t;
    t = x + y;
    return t;
}

int main(){
    std::cout << sum(5, 6) << std::endl;
    std::cout << sum(5, 6) << std::endl;
    std::cout << sum(5.4f, 6.4f) << std::endl;
    std::cout << sum(5.3, 6.3) << std::endl;
    return 0;
}
```
OR use Typename

```cpp
#include <iostream>

template<typename T>
T sum (T x , T y){
    T t;
    t = x + y;
    return t;
}

int main(){
    std::cout << sum(5, 6) << std::endl;
    std::cout << sum(5, 6) << std::endl;
    std::cout << sum(5.4f, 6.4f) << std::endl;
    std::cout << sum(5.3, 6.3) << std::endl;
    return 0;
    // it will have 3 different copies
}
```

### NOTE: After compile there will be as many copies of the template function as there are number of different call statements.

## RECURSION (Fucntion calling itself)
```cpp
#include <iostream>
int main(){
    int i = 1; // local variable / autommatic varaiable
    std::cout << "hello maya";
    i++;
    if(i > 5)
        return 0;
    main();
    return 0;
} // it is a infinite recursion
```

## SOLUTION TO RECURSION
- Static variable
 ```cpp
#include <iostream>
int main(){
    static int i = 1; // local variable / autommatic varaiable
    std::cout << "hello maya" << std::endl;
    i++;
    if(i > 5)
        return 0;
    main();
    return 0;
}
```

- global variable
```cpp
#include <iostream>
int i = 1;
int main(){
    std::cout << "hello maya" << std::endl;
    i++;
    if(i > 5)
        return 0;
    main();
    return 0;
}
```

# POINTER
- Pointer is a special variable which can store the address of any other variable.
- The type of the pointer and the variable must be same
```cpp
int a = 5;
float b = 10;
int *p;
p = &a;
p = &b;  // it will throw error or warning depends on compiler

float (*P)(int , int)   // Pointer to Function READ ABOUT IT
```
POINTER SIZE:
```cpp
#include <iostream>
int main(){
    int a;
    float b;
    long long c;
    int *d;
    float *e;
    long long *f;
    std::cout << "int: " << sizeof(a) << " int* :" << sizeof(d)
              << " float: " << sizeof(b) << " float* :" << sizeof(e)
              << " long long: " << sizeof(c) << " long long* :" << sizeof(f);
    return 0;
    // int: 4 int* :8 float: 4 float* :8 long long: 8 long long* :8
}
```
DEREFRENCING
```cpp
int a = 5;
int *p;
p = &a;
*p = 7; // DEREFENCING
cout << a;  // outputs: 7
```

PRINT ADDRESS
```c
int a = 5;
int *p;
p = &a;
cout << "address of a is: " << &a;
cout << "address of a is: "  << p;
cout << "Value of a is :  "  << a;      //5
cout << "Value of a is :  "  << *p;     //5
```

iterator is also a pointer , STL (standard template library)

- SWAP 2 NUMBERS
```cpp
#include <iostream>
int main(){
    int a, b;
    int *p1, *p2;
    p1 = &a;
    p2 = &b;
    std::cin >> a >> b;
    *p1 = (*p1) ^ (*p2);
    *p2 = (*p1) ^ (*p2);
    *p1 = (*p1) ^ (*p2);
    std::cout << "value a: " << *p1 << " value b: " << *p2;
    return 0;
}
```

`Call by reference is not is equals to call by address in c++.`
- Swap two numbers via pointers
```cpp
#include <iostream>
void sum(int *a ,int *b){
    int t;
    t = *a;
    *a = *b;
    *b = t;
}
int main(){
    int a = 5, b = 9;
    sum(&a, &b);
    std::cout << "a: " << a << " b: " << b;
    return 0;
}
```

## Limitation of Pointers
- extra memory is required
- syntax is not simple
    - SOLUTION
      - Reference / nickname
      - in C++ only

# 

|Pointer | Reference|
| ------ | ---------|
|int a = 5 | int a = 5 |
|int *p;   | int &r = a ; no extra memory required| 
| p = &a ; address of a| it is referenve or alias|
|*p = 7; need to do derefrence to change| r = 7; directly change|


### NOTE: a function can return maximum one value but using pointer it can return multiple values


# Function Pointer
```cpp
#include <iostream>

inline int add(int a , int b){
    return a + b;
}

int main(){
    int (*ptr)(int, int) = &add;
    std::cout << ptr(3, 5);
    return 0;
}
```

### Remeber int *arr[10] and int (*arr)[10] in the first one fight will be concluded depending on the precedence and we want a pointer that points to 10 interger value