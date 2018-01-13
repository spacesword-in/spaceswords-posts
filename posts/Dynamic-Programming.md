title: Dynamic Programming
author: Deven Sharma
tags: []
categories:
    - Programming
    - C++
date: 2018-01-08 05:00:00
---
<p id="icon" class="mx-auto" style="text-shadow: rgb(179, 136, 36) 0px 0px, rgb(179, 136, 36) 1px 1px, rgb(180, 137, 36) 2px 2px, rgb(181, 138, 36) 3px 3px, rgb(182, 138, 36) 4px 4px, rgb(182, 139, 36) 5px 5px, rgb(183, 139, 37) 6px 6px, rgb(184, 140, 37) 7px 7px, rgb(185, 140, 37) 8px 8px, rgb(185, 141, 37) 9px 9px, rgb(186, 142, 37) 10px 10px, rgb(187, 142, 37) 11px 11px, rgb(188, 143, 38) 12px 12px, rgb(188, 143, 38) 13px 13px, rgb(189, 144, 38) 14px 14px, rgb(190, 145, 38) 15px 15px, rgb(191, 145, 38) 16px 16px, rgb(192, 146, 38) 17px 17px, rgb(192, 146, 38) 18px 18px, rgb(193, 147, 39) 19px 19px, rgb(194, 147, 39) 20px 20px, rgb(195, 148, 39) 21px 21px, rgb(195, 149, 39) 22px 22px, rgb(196, 149, 39) 23px 23px, rgb(197, 150, 39) 24px 24px, rgb(198, 150, 40) 25px 25px, rgb(198, 151, 40) 26px 26px, rgb(199, 152, 40) 27px 27px, rgb(200, 152, 40) 28px 28px, rgb(201, 153, 40) 29px 29px, rgb(201, 153, 40) 30px 30px, rgb(202, 154, 40) 31px 31px, rgb(203, 154, 41) 32px 32px, rgb(204, 155, 41) 33px 33px, rgb(205, 156, 41) 34px 34px, rgb(205, 156, 41) 35px 35px, rgb(206, 157, 41) 36px 36px, rgb(207, 157, 41) 37px 37px, rgb(208, 158, 42) 38px 38px, rgb(208, 158, 42) 39px 39px, rgb(209, 159, 42) 40px 40px, rgb(210, 160, 42) 41px 41px, rgb(211, 160, 42) 42px 42px, rgb(211, 161, 42) 43px 43px, rgb(212, 161, 42) 44px 44px, rgb(213, 162, 43) 45px 45px, rgb(214, 163, 43) 46px 46px, rgb(214, 163, 43) 47px 47px, rgb(215, 164, 43) 48px 48px, rgb(216, 164, 43) 49px 49px, rgb(217, 165, 43) 50px 50px, rgb(218, 165, 44) 51px 51px, rgb(218, 166, 44) 52px 52px, rgb(219, 167, 44) 53px 53px, rgb(220, 167, 44) 54px 54px, rgb(221, 168, 44) 55px 55px, rgb(221, 168, 44) 56px 56px, rgb(222, 169, 44) 57px 57px, rgb(223, 170, 45) 58px 58px, rgb(224, 170, 45) 59px 59px, rgb(224, 171, 45) 60px 60px, rgb(225, 171, 45) 61px 61px, rgb(226, 172, 45) 62px 62px, rgb(227, 172, 45) 63px 63px, rgb(227, 173, 45) 64px 64px, rgb(228, 174, 46) 65px 65px, rgb(229, 174, 46) 66px 66px, rgb(230, 175, 46) 67px 67px, rgb(231, 175, 46) 68px 68px, rgb(231, 176, 46) 69px 69px, rgb(232, 177, 46) 70px 70px, rgb(233, 177, 47) 71px 71px, rgb(234, 178, 47) 72px 72px, rgb(234, 178, 47) 73px 73px, rgb(235, 179, 47) 74px 74px, rgb(236, 179, 47) 75px 75px, rgb(237, 180, 47) 76px 76px, rgb(237, 181, 47) 77px 77px, rgb(238, 181, 48) 78px 78px, rgb(239, 182, 48) 79px 79px, rgb(240, 182, 48) 80px 80px, rgb(240, 183, 48) 81px 81px, rgb(241, 184, 48) 82px 82px, rgb(242, 184, 48) 83px 83px, rgb(243, 185, 49) 84px 84px, rgb(244, 185, 49) 85px 85px, rgb(244, 186, 49) 86px 86px, rgb(245, 186, 49) 87px 87px, rgb(246, 187, 49) 88px 88px, rgb(247, 188, 49) 89px 89px, rgb(247, 188, 49) 90px 90px, rgb(248, 189, 50) 91px 91px, rgb(249, 189, 50) 92px 92px, rgb(250, 190, 50) 93px 93px, rgb(250, 191, 50) 94px 94px, rgb(251, 191, 50) 95px 95px, rgb(252, 192, 50) 96px 96px, rgb(253, 192, 51) 97px 97px, rgb(253, 193, 51) 98px 98px, rgb(254, 193, 51) 99px 99px; font-size: 147px; color: rgb(255, 255, 255); background-color: rgb(255, 194, 51); height: 282px; width: 282px; line-height: 282px; border-radius: 0%; overflow: hidden; text-align: center;">DP</p>
## Dynamic Programming 

   As it is said that "Those who could not remember the past are condemned to repeat it".
   
   Dynamic Programming is one of the most beautiful form of algorithm .Its an intution based technique.In this we reduce the exponential complexity to the polynomial complexity.This artical actually focuces on the understanding of the dynamic programming not the algorithm.
   
   What my approach is that i want to develop the intution of the dynamic programming.First we need to develop the recursive algorithm and then the bottom up approach.Understanding is must in the dynamic programming not learnig  the algorithm .
   
   ## Approaches to dynamic programming 
   
   ### Topdown Approach
   In this approach we  start building the recursive solution i.e we move to the base case and then start building the solution its not exact definition but just for the understanding
   ### Bottom up Approach
   We try to develop the iterative solution 
   
  #### MEMOIZATION NOT MEMORIZATION
  
   Memoization ensures that a method doesn't run for the same inputs more than once by keeping a record of the results for the given inputs.
   
   ### Lets see an example:
   
   ```C++
   # include <iostream>
   using namespace std;
int fib(int n )
{
if(n==0 || n==1 )
return 1;
else
return fib(n-1)+fib(n-2);
}
int main()
   {
   fib(5);
   }
     
  
  ///output produced is as 
  5
  

    ```
    
 Lets see how does the memoization work
 
 ![fibonaaci](https://www.interviewcake.com/images/svgs/fibonacci__binary_tree_recursive.svg?bust=161)
 Now see here above fib(1)  and fib(0) is calculated 4 and  3 times respectively so we can precompute their result and store that result and when we want to use that result we just need to return that value.Once calculated we do not need to  calculate that result again and again.
 
 ```C++
 # include <bits/stdc++.h>
using namespace std;
int dp[100];//array for storing the result
int fib(int n)
{
	if(dp[n]!=-1)//check if array is filled or not if filled then return the result
		return dp[n];
	else if(n == 0 || n==1)
		return n;
	else
		return fib(n-1)+fib(n-2);
	dp[n]=n;


}
 int main()

{
	memset(dp,-1 ,sizeof(dp));
	cout<<fib(10);
}
 ```
 ##### HOW DOES THIS WORK
 ![fib](https://github.com/Sdev0245/Images/blob/master/IMG_20180108_113005.jpg?raw=true)
 
 ## State in Dynamic Programming
  The state in dp is one of the most important thing once you can generate the state then you can easily solve the dynamic programming question
  The "State" is actually the way of defining the solution to the sub problem.We need to break the problem to smaller states and then solve them.
  
  ## Overlapping Subproblem
   We have the overlapping subproblem means we are computing the same solution again and again as above in fibonacci program .
 
 ## Optimal substructue
   If an optimal solution can be constructed from optimal solutions of its subproblems is called as optimal substructure.
  <div style="background-color:white;">
  ![Optimal](https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Shortest_path_optimal_substructure.svg/1200px-Shortest_path_optimal_substructure.svg.png)
  </div>
  
  As above in the diagram we are not moving greedily 
  we are also considering each path very carefully this is optimal substructure.Not taking  the 2's path 
  We are considering the path from 5 to 20 = 25 , 2+25=27 ,11+17=28.
  
  ### How to know whether the problem is related to Dynamic programming?
  
  In the most of the cases you are asked to maximize or minimize the solution in that case you need to use the dynamic programming.The mathematics play a great role in the dynamic programming you need to form the formulae for the realtion among the states 
  
#### Lets see one of the questions of SPOJ for better understanding.
 
[ACPC10D - Tri graphs](http://www.spoj.com/problems/ACPC10D/)

   

Here’s a simple graph problem: Find the shortest path from the top-middle vertex to the bottom-middle vertex in a given tri-graph. A tri-graph is an acyclic graph of (N ≥ 2) rows and exactly 3 columns. Unlike regular graphs, the costs in a tri-graph are associated with the vertices rather than the edges.

![](http://www.spoj.com/content/omar_azazy:ACPC10D)
So, considering the example with N = 4, the cost of going straight down from the top to bottom along the middle vertices is 7 + 13 + 3 + 6 = 29. The layout of the directional edges in the graph are always the same as illustrated in the figure.

#### Input
Your program will be tested on one or more test cases.
Each test case is specified using N + 1 lines where the first line specifies a single integer (2 ≤ N ≤ 100, 000) denoting the number of rows in the graph. N lines follow, each specifying three integers representing the cost of the vertices on the ith row from left to right. The square of each cost value is less than 1,000,000.
The last case is followed by a line with a single zero.

#### Output
For each test case, print the following line:
k. n
Where k is the test case number (starting at one,) and n is the least cost to go from the top-middle vertex to the bottom-middle vertex.

###### Example
###### Input:
4

13  7  5

7  13  6

14  3  12

15  6  16

0

###### Output:
  1. 22
          
   
   ##### SOLUTION:
   a[][] as INPUT array and dp[][] as the minimum distance array.
   
   As from  above we are asked to minimize the distance to move from a[0][1] to to a[n][1].Think yourself and try to deduce the formula.This needs a simple logic.
   As we cannot move from a[0][0] so it will remain as it is but not at a[0][1] , we can move to four indecies i.e But the first row is special case in out dp[][] array we will put its first row as it is except d[0][2]=a[0][1]+a[0][2]; 
  
  ###### NOTE:
  a[i][j] represent path from i to j.Index Starts from zero.
  
  For better understanding see the image carefully below
   ![](https://github.com/Sdev0245/Images/blob/master/IMG_20180108_130633.jpg?raw=true)
    So what the formula becomes:
    
    
  dp[1][0]=a[1][0]+min(dp[0][1],dp[0][0])
  
  dp[1][1]= a[1][1]+min(dp[0][0],dp[1][0],dp[1][1],dp[0][2])
  
  dp[1][2]=a[1][2]+min(dp[0][2],dp[0][1],dp[1][1])
  
  
  #### Lets see the Implementation
    C++ code:
  ```c++
# include <bits/stdc++.h>
# define ll long long 
using namespace std;
ll mini(ll x ,ll y  ,ll z);//for minimum of three elements
ll mini(ll x,ll y,ll z  ,ll k)//for minimum of four
{
	ll max=ULONG_MAX;
	if(x<=y)
		max=x;
	else 
		max=y;
	ll max2=ULONG_MAX;
	if(k>=z)
		max2=z;
	else
		max2=k;
	if(max2>=max)
		return max;
	else
		return max2;
}
ll mini(ll x ,ll y  ,ll z)
{ll max=ULONG_MAX;
	if(x>=y)
		max=y;
	else
		max=x;
	if(max>=z)
		return z;
	else
		return max;


}
int  main()
{
	
	ll  cntr=0;
	while(1)
	{
	ll n;
	cin>>n;
	if(n==0)
		break;

		++cntr; //counter variable
	ll a[n+1][3];
	ll cost[n+1][3];
	for(ll  i= 0  ;i< 3 ;i++)
	{
		for( ll j= 0 ; j<n ; j++)
			cost[i][j]=0;
	}

	for(ll  i =0 ; i< n ; i++)
	{
		for( ll j= 0 ;j< 3 ;j++ )
			scanf("%lld",&a[i][j]);
	}
	cost[0][0]=LONG_MAX;
	cost[0][1]=a[0][1];
	cost[0][2]=a[0][1]+a[0][2];
	for(ll i =1 ; i< n ;i++)
	{
		for(ll j =0 ; j< 3 ;j++)
		{
			if(j==0)
			{
				cost[i][0]=a[i][0]+min(cost[i-1][0],cost[i-1][1]);
			}
			else if(j==1)
			{
				cost[i][1]=a[i][1]+mini(cost[i-1][0],cost[i][0],cost[i-1][1],cost[i-1][2]);
			}
			else
			{
				cost[i][2]=a[i][2]+mini(cost[i][1],cost[i-1][2],cost[i-1][1]);
			}
		}
	}

			 printf("%lld.",cntr);
   printf(" %lld\n",cost[n-1][1]);//cost[n-1][1] as started index from zero
}
}
  
  
  ```
  
  ##### Article by :Deven Sharma
