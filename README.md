Smallest Subarray with sum greater than a given value in C
Here, in this page we will discuss the program to find the smallest subarray with sum greater than a given value in C programming language. If such subarray is present then print true otherwise print false.

Smallest Subarray with sum greater than a given value in C
Example :
Input : {1, 4, 45, 6, 0, 19}, value = 51
Output : 3
Explanation : Minimum length subarray is {4, 45, 6} have length = 3
While loop in C
Algorithm:
Take a variable to store the desired smallest subarray length say it is length = n.
Run a outer loop for index 0 to n.
Run a nested loop from index i+1 to n,
Find sum, if sum is equal to value, then set length = min(length, (j-i+1))
min() function will return the minimum value among the two parameters passed to it.
After complete iteration print the value of length.
Time and Space Complexity
Time Complexity : O(n2)
Space Complexity : O(1)
Run
#include <stdio.h>

int min(int a, int b){
    if(a>b)
        return b;
    
    return a;
}

int main(){
    int arr[] = {1, 4, 45, 6, 0, 19};
    int n = sizeof(arr)/sizeof(arr[0]);
    int value = 51;
    int length = n;
    
    for(int i=0; i<n; i++){
        int curr_sum = 0;
        for(int j=i; j<n; j++){ curr_sum += arr[j]; if(curr_sum > value){
                length = min(length, (j-i+1));
                break;
            }
        }
    }
    
    printf("%d", length);
    
}
Output
3
Related Pages
Find factorial of a Large Number 

Merge 2 sorted arrays without using extra space.

Find all pairs on integer array whose sum is equal to given number 

Kadane’s Algorithm

Find longest consecutive subsequence 

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
While loop in C
