# DSA
Reverse order( ABCD=DCBA_
#include<iostream>
#include<vector>
using namespace std;

int main(){
    int n;
    cin >> n;
    vector<char> arr(n);
    
    for(int i=0; i< n;i++);
    {
        cin >> arr[i];
    }
    for(int i=n-i; i>=0; i--);
    {
        cout << arr[i];
    }
     if( i>0){
         cout<<" ";
     }
     return 0;
}
