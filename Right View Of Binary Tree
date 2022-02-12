// C++ program to print left view of
// Binary Tree

#include <bits/stdc++.h>
using namespace std;

// A Binary Tree Node
struct Node {
	int data;
	struct Node *left, *right;
};

// Utility function to create a new tree node
Node* newNode(int data)
{
	Node* temp = new Node;
	temp->data = data;
	temp->left = temp->right = NULL;
	return temp;
}

// function to print Right view of
// binary tree
void printRightView(Node* root)
{
	if (root == NULL)
		return;

	queue<Node*> q;
	q.push(root);

	while (!q.empty()) {
		// get number of nodes for each level
		int n = q.size();

		// traverse all the nodes of the current level
		while (n--) {

			Node* x = q.front();
			q.pop();

			// print the last node of each level
			if (n == 0) {
				cout << x->data << " ";
			}
			// if left child is not null push it into the
			// queue
			if (x->left)
				q.push(x->left);
			// if right child is not null push it into the
			// queue
			if (x->right)
				q.push(x->right);
		}
	}
}

// Driver code
int main()
{
	// Let's construct the tree as
	// shown in example

	Node* root = newNode(1);
	root->left = newNode(2);
	root->right = newNode(3);
	root->left->left = newNode(4);
	root->left->right = newNode(5);
	root->right->left = newNode(6);
	root->right->right = newNode(7);
	root->right->left->right = newNode(8);

	printRightView(root);
}

// This code is contributed by
// Snehasish Dhar
