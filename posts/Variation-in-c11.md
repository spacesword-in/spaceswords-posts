title: Variation in c11
author: Deven sharma
tags:
  - C++
  - Competitive Programing
categories: 
  - Programming
  - C++
date: 2017-11-13 13:19:00
---
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1200px-ISO_C%2B%2B_Logo.svg.png" width="200"/>
## C++ is growing 

We all feel that writing the code in the c++ is very difficult compared to python but now the c++ is even becoming more easier as compared to the earlier c.
  Now we can actually excess the array in  some different way.
  ```c++
  # include <bits/stdc++.h>
  using namespace std;
  int main()
  {
  int n;
  cin>>n;
  int *a =new int[n];
  for(int i =0 ; i< n; i++)
  cin>>a[i];//older c++ 
  for(int  j= 0 ;j< n ;j++)
  cout<<a[j]<<endl;
  }
  ```
  
  But now it has changed as 
  array<int ,5> of type int and size 5 but remains static  
  ```c++
  # include <bits/stdc++.h>
using namespace std;
int main()
{
	array <int,5>a;//array of size 5;
	for(int i =0 ;i<5; i++)
	cin>>a[i];
    for(auto &i :a)//modern c11 way to printing auto iterator
	cout<<i<<endl;
}```
