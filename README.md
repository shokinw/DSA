# DSA
**inserting and sorting**
Reverse order( ABCD=DCBA)
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
<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**inserting sorting**

#include<iostream>
#include<vector>
using namespace std;

int main(){
    int n;
    cin >> n;
    vector<int> product(n);
    for(int i=0; i<n;i++){
        cin>> product[i];
    }
    bool first =true;
    for(int i=0;i<n;i++){
        if(product[i]!=0){
            if(!first){
                cout<<" ";
            }
            cout<< product[i];
            first=false;
        }
    }
    return 0;
    
}

<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
