# potd-solution
                                                           COUNT OF SUBARRAYS(POTD)
Given an array of N positive integers  Arr1, Arr2 ............ Arrn. The value of each contiguous subarray of given array is the maximum element present in that subarray. The task is to return the number of subarrays having value strictly greater than K.

Example 1:

Input:
N = 3, K = 2
Arr[] = {3, 2, 1}
Output: 3
Explanation: The subarrays having value
strictly greater than K are: [3], [3, 2]
and [3, 2, 1]. Thus there are 3 such
subarrays.
Example 2:

Input:
N = 4, K = 1
Arr[] = {1, 2, 3, 4}
Output: 9
Explanation: There are 9 subarrays having
value strictly greater than K.
Your Task:
Complete the function countSubarray() which takes an array arr, two integers n, k, as input parameters and returns an integer denoting the answer. You don't to print answer or take inputs.

Expected Time Complexity: O(N)
Expected Auxiliary Space: O(1)

Constraints:
1 <= N <= 105
1 <= Arr[i] <= 105
for(int i = 0 ; i < n ; i++){
    if(arr[i]>k){
       ans+=c*(c+1)/2;
        c=0;//first write this then go to elseand then come bak to this if loop to understand serially
    }
    else{
        //when current value <=k
        c++;//no. of elements that are <=k //ab ye khi store to nhi horha filhal to ise store krne ke liye ans rakhenge if me and outside the loop
    }
    
}
ans+=c*(c+1)/2;
	   return n*(n+1)/2 - ans; 
	}
};

//{ Driver Code Starts.

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n, k, i;
        cin >> n >> k;
        int arr[n];
        for (i = 0; i < n; i++) {
            cin >> arr[i];
        }
        Solution ob;
        auto ans = ob.countSubarray(arr, n, k);
        cout << ans << "\n";
    }
    return 0;
}
// } Driver Code Ends
