

#include <iostream>
using namespace std;

class Node{
    public:
    int data;
    Node* next;

    Node(int data) {
        this-> data = data;
        this -> next = NULL;
    }
};

// insert at beg
void insertathead(Node* &head, int d) { 
    Node* temp = new Node(d);
    temp -> next = head;
    head = temp;
}

void print(Node* &head) {
    Node* temp = head;

    while(temp != NULL) {
        cout << temp->data << " ";
        temp = temp-> next;
    }
    cout << endl;
}


int main() {
    Node* node1= new Node(10);                
   // cout << node1 -> data << endl;    // 10
   // cout << node1 -> next<< endl;     // 0

    Node* head = node1;
    print(head);              // 10

    insertathead(head,12);
    print(head);   // 12 10
   

    
    insertathead(head,15);
    print(head);       // 15 12 10
 
    
    return 0;
}
