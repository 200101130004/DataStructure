// C++ program to partition a linked list around a
// given value.
#include<bits/stdc++.h>
using namespace std;

/* Link list Node */
struct Node
{
	int data;
	struct Node* next;
};

// A utility function to create a new node
Node *newNode(int data)
{
	struct Node* new_node = new Node;
	new_node->data = data;
	new_node->next = NULL;
	return new_node;
}

// Function to make a new list(using the existing
// nodes) and return head of new list.
struct Node *partition(struct Node *head, int x)
{
	/* Let us initialize start and tail nodes of
	new list */
	struct Node *tail = head;

	// Now iterate original list and connect nodes
	Node *curr = head;
	while (curr != NULL)
	{
		struct Node *next = curr->next;
		if (curr->data < x)
		{
			/* Insert node at head. */
			curr->next = head;
			head = curr;
		}

		else // Append to the list of greater values
		{
			/* Insert node at tail. */
			tail->next = curr;
			tail = curr;
		}
		curr = next;
	}
	tail->next = NULL;

	// The head has changed, so we need
	// to return it to the user.
	return head;
}

/* Function to print linked list */
void printList(struct Node *head)
{
	struct Node *temp = head;
	while (temp != NULL)
	{
		printf("%d ", temp->data);
		temp = temp->next;
	}
}

// Driver program to run the case
int main()
{
	/* Start with the empty list */
	struct Node* head = newNode(3);
	head->next = newNode(5);
	head->next->next = newNode(8);
	head->next->next->next = newNode(2);
	head->next->next->next->next = newNode(10);
	head->next->next->next->next->next = newNode(2);
	head->next->next->next->next->next->next = newNode(1);

	int x = 5;
	head = partition(head, x);
	printList(head);
	return 0;
}
