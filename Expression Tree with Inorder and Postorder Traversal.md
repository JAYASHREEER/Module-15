Ex. No: 15C - Expression Tree with Inorder and Postorder Traversal

AIM:
To write a Python program to build the given expression tree and print the inorder and postorder traversals.

ALGORITHM:
 Input Postfix Expression
Accept a postfix expression as a string (e.g., "3 4 + 2 * 7 /").

Split the expression into tokens (operands and operators).

📌 Step 2: Define Expression Tree Node
Define a class Node with:

value: stores operand/operator.

left and right: left and right children.

📌 Step 3: Build Expression Tree
Initialize an empty stack.

For each token in the postfix expression:

If the token is an operand:

Create a node and push it to the stack.

If the token is an operator:

Pop two nodes from the stack.

Create a new node with the operator.

Assign the second popped node as left child and the first popped node as right child.

Push the new node back to the stack.

After processing all tokens, the stack’s top is the root of the expression tree.

📌 Step 4: Traversals
Inorder Traversal:

Recursively:

Traverse left subtree.

Visit root.

Traverse right subtree.

Add parentheses to preserve expression order.

Postorder Traversal:

Recursively:

Traverse left subtree.

Traverse right subtree.

Visit root.

📌 Step 5: Output
Print the inorder traversal (infix notation with parentheses).

Print the postorder traversal (postfix expression).



PROGRAM:

```
from binarytree import build
node=[1,2,3,4,5,6,7,8,None,None,None,9,10]
root=build(node)
for i in root.values:
    print(i,"--> ",end="")
print("\nThe postorder is ",root.postorder)
```
OUTPUT
![image](https://github.com/user-attachments/assets/4403b6b8-6443-4bb6-a910-b1842b3879e9)

RESULT
Thus, the  Python program to build the given expression tree and print the inorder and postorder traversals was successfully implemented and verified.
