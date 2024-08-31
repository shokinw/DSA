# DSA
**inserting and sorting**
?? program that removes out-of-stock products from the array.
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
? program that removes out-of-stock products from the array.
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

**insertion and deletion**
? how many words in a list start with a specific letter!!


#include<iostream>
#include<string>
using namespace std;

int main(){
    int n;
    cin >> n;
    
    string word[n];
    for(int i=0;i<n; i++){
        cin>> word[i];
    }
    
    char letter;
    cin >> letter;
    
    int count=0;
    
    for( int i=0; i< n; i++){
        if( word[i][0]== letter){
            count++;
        }
    }
        cout << count << endl;
