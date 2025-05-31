# Ex12 Binary Search Tree

## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. Start
2. Check if the current node is NULL; if true, create a new node with the given key.
3. Allocate memory for the new node, set its key, and initialize its left and right children to NULL.
4. If the current node is not NULL, compare the key with the current node's key.
5. If key <= node->key, recursively insert the key into the left subtree and update the left child pointer.
6. If key > node->key, recursively insert the key into the right subtree and update the right child pointer.
7. Return the current node after the insertion.
8. End  

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: SUBHASHINI.B
RegisterNumber:  212223040211
*/
/*structnode{ int key;
struct node*left, *right;
};*/
struct node* insert(struct node* node, int key)
{
if(node==NULL)
{
struct node* node=(struct node*)malloc(sizeof(struct node)); node->key=key;
node->left=NULL; node->right=NULL; returnnode;
}
else
{
struct node* cur; if(key<=node->key)
{
cur=insert(node->left,key); node->left=cur;
}

else
{
cur=insert(node->right,key); node->right=cur;
}
returnnode;
}
}

```

## Output:

![Screenshot 2025-04-29 111021](https://github.com/user-attachments/assets/a4b055da-5240-4093-b58a-485f504ec8cd)


## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
