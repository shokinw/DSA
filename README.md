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



<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**important code to learn linked list**
#include<iostream>
using namespace std;

struct node
{
int data;
struct node* next;

node(int val)
{
data = val;
next = NULL;
}
};

struct node* insertAtHead(node* head, int val) {
node* n = new node(val);
n->next = head;
head = n;
return head;
}

struct node* insertAtLast(node* head, int val) {
node* n = new node(val);
if (head == NULL) {
head = n;
return head;
}
node* temp = head;
while (temp->next != NULL) {
temp = temp->next;
}
temp->next = n;
return head;
}

struct node* insertAtPosition(node* head, int val, int pos) {
if (pos == 1) {
return insertAtHead(head, val);
}

node* n = new node(val);
node* temp = head;

// Move temp to the node before the position
for (int i = 1; i < pos - 1; i++) {
if (temp == NULL) {
cout << "Position out of bounds." << endl;
return head;
}
temp = temp->next;
}

if (temp == NULL || temp->next == NULL && pos != 2) {
cout << "Position out of bounds." << endl;
return head;
}

n->next = temp->next;
temp->next = n;

return head;
}

void display(node* head)
{
node* temp = head;
while(temp!=NULL){
cout << temp->data << "->";
temp = temp->next;
}
cout <<"NULL" << endl;
}

struct node* deleteAtHead(node* head)
{
node* temp = head;
head = head->next;
delete temp;
return head;
}

struct node* deleteAtLast(node* head) {
if (head == NULL) {
cout << "List is empty, nothing to delete." << endl;
return head;
}
if (head->next == NULL) {
delete head;
return NULL;
}
node* temp = head;
while (temp->next->next != NULL) {
temp = temp->next;
}
delete temp->next;
temp->next = NULL;
return head;
}

struct node* deleteAtPosition(node* head, int pos) {
if (head == NULL) {
cout << "List is empty, nothing to delete." << endl;
return head;
}
if (pos == 1) {
return deleteAtHead(head);
}
node* temp = head;
node* prev = NULL;
for (int i = 1; i < pos; i++) {
if (temp->next == NULL || temp->next->next == NULL) {
cout << "Position out of bounds." << endl;
return head;
}
prev = temp;
temp = temp->next;
}
prev->next = temp->next;
delete temp;
return head;
}


int main(){

node* head = NULL;
head = insertAtHead(head,4);
head = insertAtHead(head,8);
head = insertAtHead(head,2);
head = insertAtHead(head,1);
head = insertAtLast(head,7);
head = insertAtLast(head,9);
head = insertAtPosition(head,10,4);
head = insertAtPosition(head,12,2);
display(head);
head = deleteAtHead(head);
display(head);
head = deleteAtLast(head);
display(head);
head = deleteAtPosition(head,2);
display(head);
return 0;
}
