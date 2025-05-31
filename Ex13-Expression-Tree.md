# Ex13 Expression Tree
## AIM:
To write a C function to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.

## Algorithm
1. Start
2. Print node data in preorder then traverse left then right
3. Traverse left in inorder then print node data then traverse right.
4. Traverse left in postorder then traverse right then print node data
5. Recursive approach is used for all three traversal methods
6. Functions handle each tree node using tree->d, tree->l, tree->r
7. End  

## Program:
```
/*
Program to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.
Developed by: SUBHASHINI.B  
RegisterNumber: 212223040211 
*/
/*
struct n { char d; struct n*l; struct n*r;
};*/
voidpreOrder(struct n*tree)
{
if(tree)
{
printf("%c",tree->d); preOrder(tree->l); preOrder(tree->r);
}
}
void inOrder(struct n*tree)
{
if(tree)
{
inOrder(tree->l); printf("%c",tree->d); inOrder(tree->r);
}
}
voidpostOrder(struct n*tree)

{
if(tree)
{
postOrder(tree->l); postOrder(tree->r); printf("%c",tree->d);
}
}
```

## Output:

![Screenshot 2025-04-29 111242](https://github.com/user-attachments/assets/a611a0f6-89d8-4b66-afde-817bb72cbcc1)



## Result:
Thus, the C program to display the Expression Tree in the format of In-order ,Pre-order and Post-order traversal.
