#include<iostream>
using namespace std;

// Structure of a node

struct Node
{
	
	//Feilds in a node.

	//First field --> Data

	int data;

	//Second field --> next(which contains address)
	
	Node *next;

	/*Second feild is of type Node* ?
	because the next node is also of type Node which will also contain data and next field into it.
	thats why the type of next filed is Node*. */	
};

// function for creation of Node.
// It is of type Node* because we gonna return a node from this function.
Node* newNode(int data)
{
	//First of all create new node using new keyword (new keyword is used for dynamic memory allocation).
	Node *nn = new Node;
	nn->data = data ; // put the value coming in data argument in the data feild.
	nn->next = NULL; // next of new node is assign to NULL.

	// now our node is created succesfully , let's return it to the caller.

	return nn;
}

void insert(Node *&head , int data)
{
	//While inserting a new node , first check if the node(List) is NULL.
	if(head == NULL)
	{
		head = newNode(data); // function call to newNode() function.
	}
	
	/*If the node is not then , we already have some nodes in our linked list so go ahead and create new one to 	insert*/

	Node *nn = newNode(data); // notice here we are calling a function for creating a node.
	
	nn->next = head;
	head = nn; 	
}

void deleteNode(Node* head)
{
	Node *cn  = head;
	while(cn->next->next != NULL)
	{
		cn = cn->next;
	}

	delete(cn);
}

// Function to print linked list.
void printList(Node*head)
{
	Node *cn = head;
	while(cn->next!=NULL)
	{
		cout<<cn->data<<"-->";
		cn = cn->next;
	}
	cout<<"NULL"<<endl;
}
/* main function (Entry point of a program)*/
int main()
{
	//Every linked list has a head node. so,  we will first create head node and initialize it with NULL.

	Node *head = NULL;

	// function to insert data into Linked List.
	insert(head,1);
	insert(head,2);
	insert(head,3);

	// function call for print list.
	printList(head);

	//delete last node.

	deleteNode(head);

	printList(head);

	
}
