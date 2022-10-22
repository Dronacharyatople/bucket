//{ Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

// } Driver Code Ends
class Solution {
  public:
    int fillingBucket(int N) {
        int max=100000;
     int arr[max];
     arr[0]=1;
     arr[1]=2;
     for(int i=2;i<max;i++)
     {
         arr[i]=(arr[i-1]+arr[i-2])%100000000;
     }
     return arr[N-1]%100000000;
    }
};

//{ Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int N;
        
        cin>>N;

        Solution ob;
        cout << ob.fillingBucket(N) << endl;
    }
    return 0;
}
// } Driver Code Ends
