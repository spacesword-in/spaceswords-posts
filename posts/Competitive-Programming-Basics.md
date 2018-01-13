title: Competitive Programming  Basics
author: Deven Sharma
tags:
  - Competitive
categories: 
    - Programming
    - C++
date: 2017-11-09 06:25:00
---
![coding](https://i.imgur.com/jx13itM.png)
#### Taking input till the End of file
#### Multiple Test Cases
In a programming contest problem, the correctness of your code is usually determined by
running your code against several test cases. Rather than using many individual test case
files, modern programming contest problems usually use one test case file with multiple test
cases included. In this section, we use a very simple problem as an example of a multiple-
test-cases problem: Given two integers in one line, output their sum in one line. We will
illustrate three possible input/output formats:
• The number of test cases is given in the first line of the input.
• The multiple test cases are terminated by special values (usually zeroes).
• The multiple test cases are terminated by the EOF (end-of-file) signal.
``` c++
#include <iostream>
using namespace std;
using ll =long long ;//one way to use the namespaces defined ll as the long long 
int main(){
	
    //if you have the input file in case of the competitive proramming 
    ll n;
    while(scanf("%lli",&n)!=EOF)//returns the no of the arguments 
    {
    
    //do some task
    
}
    
}

```
##### Use of the fast input as fast as the scanf
#### Fast I/O for Competitive Programming
2.2
In competitive programming, it is important to read input as fast as possible so we save valuable time.

You must have seen various problem statements saying: “Warning: Large I/O data, be careful with certain languages (though most should be OK if the algorithm is well designed)”. Key for such problems is to use Faster I/O techniques.

It is often recommended to use scanf/printf instead of cin/cout for a fast input and output. However, you can still use cin/cout and achieve the same speed as scanf/printf by including the following two lines in your main() function:

    ios_base::sync_with_stdio(false);
It toggles on or off the synchronization of all the C++ standard streams with their corresponding standard C streams if it is called before the program performs its first input or output operation. Adding ios_base::sync_with_stdio (false); (which is true by default) before any I/O operation avoids this synchronization. It is a static member of function of std::ios_base.

    cin.tie(NULL);
tie() is a method which simply guarantees the flushing of std::cout before std::cin accepts an input. This is useful for interactive console programs which require the console to be updated constantly but also slows down the program for large I/O. The NULL part just returns a NULL pointer.
```c++
#include <iostream>
using namespace std;
using ll =long long ;//one way to use the namespaces defined ll as the long long 
int main(){
ios_base::sync_with_stdio(0);
cin.tie(0);
}
```
