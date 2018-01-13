title: 'MACROS KING '
author: Team SpaceSword
date: 2017-11-09 07:29:22
tags:
categories: 
  - Programming
  - C++
---
<p id="icon" class="mx-auto" style="text-shadow: rgb(64, 179, 163) 0px 0px, rgb(65, 179, 164) 1px 1px, rgb(65, 180, 164) 2px 2px, rgb(65, 181, 165) 3px 3px, rgb(66, 182, 166) 4px 4px, rgb(66, 182, 167) 5px 5px, rgb(66, 183, 167) 6px 6px, rgb(66, 184, 168) 7px 7px, rgb(67, 185, 169) 8px 8px, rgb(67, 185, 169) 9px 9px, rgb(67, 186, 170) 10px 10px, rgb(67, 187, 171) 11px 11px, rgb(68, 188, 171) 12px 12px, rgb(68, 188, 172) 13px 13px, rgb(68, 189, 173) 14px 14px, rgb(69, 190, 174) 15px 15px, rgb(69, 191, 174) 16px 16px, rgb(69, 192, 175) 17px 17px, rgb(69, 192, 176) 18px 18px, rgb(70, 193, 176) 19px 19px, rgb(70, 194, 177) 20px 20px, rgb(70, 195, 178) 21px 21px, rgb(70, 195, 178) 22px 22px, rgb(71, 196, 179) 23px 23px, rgb(71, 197, 180) 24px 24px, rgb(71, 198, 181) 25px 25px, rgb(72, 198, 181) 26px 26px, rgb(72, 199, 182) 27px 27px, rgb(72, 200, 183) 28px 28px, rgb(72, 201, 183) 29px 29px, rgb(73, 201, 184) 30px 30px, rgb(73, 202, 185) 31px 31px, rgb(73, 203, 185) 32px 32px, rgb(74, 204, 186) 33px 33px, rgb(74, 205, 187) 34px 34px, rgb(74, 205, 188) 35px 35px, rgb(74, 206, 188) 36px 36px, rgb(75, 207, 189) 37px 37px, rgb(75, 208, 190) 38px 38px, rgb(75, 208, 190) 39px 39px, rgb(75, 209, 191) 40px 40px, rgb(76, 210, 192) 41px 41px, rgb(76, 211, 192) 42px 42px, rgb(76, 211, 193) 43px 43px, rgb(77, 212, 194) 44px 44px, rgb(77, 213, 195) 45px 45px, rgb(77, 214, 195) 46px 46px, rgb(77, 214, 196) 47px 47px, rgb(78, 215, 197) 48px 48px, rgb(78, 216, 197) 49px 49px, rgb(78, 217, 198) 50px 50px, rgb(78, 218, 199) 51px 51px, rgb(79, 218, 199) 52px 52px, rgb(79, 219, 200) 53px 53px, rgb(79, 220, 201) 54px 54px, rgb(80, 221, 202) 55px 55px, rgb(80, 221, 202) 56px 56px, rgb(80, 222, 203) 57px 57px, rgb(80, 223, 204) 58px 58px, rgb(81, 224, 204) 59px 59px, rgb(81, 224, 205) 60px 60px, rgb(81, 225, 206) 61px 61px, rgb(82, 226, 206) 62px 62px, rgb(82, 227, 207) 63px 63px, rgb(82, 227, 208) 64px 64px, rgb(82, 228, 209) 65px 65px, rgb(83, 229, 209) 66px 66px, rgb(83, 230, 210) 67px 67px, rgb(83, 231, 211) 68px 68px, rgb(83, 231, 211) 69px 69px, rgb(84, 232, 212) 70px 70px, rgb(84, 233, 213) 71px 71px, rgb(84, 234, 213) 72px 72px, rgb(85, 234, 214) 73px 73px, rgb(85, 235, 215) 74px 74px, rgb(85, 236, 216) 75px 75px, rgb(85, 237, 216) 76px 76px, rgb(86, 237, 217) 77px 77px, rgb(86, 238, 218) 78px 78px, rgb(86, 239, 218) 79px 79px, rgb(86, 240, 219) 80px 80px, rgb(87, 240, 220) 81px 81px, rgb(87, 241, 220) 82px 82px, rgb(87, 242, 221) 83px 83px, rgb(88, 243, 222) 84px 84px, rgb(88, 244, 223) 85px 85px, rgb(88, 244, 223) 86px 86px, rgb(88, 245, 224) 87px 87px, rgb(89, 246, 225) 88px 88px, rgb(89, 247, 225) 89px 89px, rgb(89, 247, 226) 90px 90px, rgb(90, 248, 227) 91px 91px, rgb(90, 249, 227) 92px 92px, rgb(90, 250, 228) 93px 93px, rgb(90, 250, 229) 94px 94px, rgb(91, 251, 230) 95px 95px, rgb(91, 252, 230) 96px 96px, rgb(91, 253, 231) 97px 97px, rgb(91, 253, 232) 98px 98px, rgb(92, 254, 232) 99px 99px; font-size: 75px; color: rgb(255, 255, 255); background-color: rgb(92, 255, 233); height: 285px; width: 285px; line-height: 285px; border-radius: 0%; overflow: hidden; text-align: center;">Macros</p>
## BE THE KING OF MACROS 
MACROS IN C++


In a C program, all lines that start with # are processed by preprocessor which is a special program invoked by the compiler. In a very basic term, preprocessor takes a C program and produces another C program without any #.

Following are some interesting facts about preprocessors in C.

1) When we use include directive,  the contents of included header file (after preprocessing) are copied to the current file.

Angular brackets < and > instruct the preprocessor to look in the standard folder where all header files are held.  Double quotes “ and “ instruct the preprocessor to look into the current folder and if the file is not present in current folder, then in standard folder of all header files.

2) When we use define for a constant, the preprocessor produces a C program where the defined constant is searched and matching tokens are replaced with the given expression. For example in the following program max is defined as 100.
```
c++
#include<stdio.h>
#define max 100
int main()
{
    printf("max is %d", max);
    return 0;
}
// Output: max is 100
// Note that the max inside "" is not replaced
```
This code below shows the use of macro like a functions as the macros but the mcros donot return any value and they are faster to excess so we can replace any statement by macro that doesnot return any value.
In order to do that we need to place \ after the statement and enclose them in the braces.
at the end statement we dont need to place \.


``` c++
# include <bits/stdc++.h>
# define temp(n)\
{\
for(int i =0 ;i< n; i++)\
cout<<i<<endl;}//macro defined faster excess for loop inside the macro
using namespace std;
int main()
{
	temp(10);// macro called 

}



```
The C syntax only allows expressions to be separated by the comma operator (,). do ... while() is not an expression, but a statement, so it is an error to use it as a value to a comma operator.

Generally speaking, an inline function should be preferred over a macro to perform some inline computation. They are easier to implement, less error prone, and easier to maintain. There are very few situations where an inline function would fail where a macro would succeed.

There really isn't a safe macro to achieve your objective, but a workaround would be to pass the variable you want updated in as a macro parameter.

```
c++
#define FOO(x, y, result) \
    do { \
        do { \
            --x; \
            ++y; \
        } while(x > y); \
        result = x * y; \
    } while(0)
    ```
