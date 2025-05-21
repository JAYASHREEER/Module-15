Ex. No: 15E - Build and Evaluate an Expression Tree

AIM:
To write a Python program to build and evaluate the given Expression tree.

ALGORITHM:
Step 1: Input Collection
Accept a postfix expression (e.g., "3 4 + 2 * 7 /").

Split the expression into tokens (operands and operators).

📌 Step 2: Define Node Structure
Define a Node class with:

value → to store operand or operator.

left and right → pointers to child nodes.

📌 Step 3: Build the Expression Tree
Initialize an empty stack.

For each token in the postfix expression:

If operand:

Create a node with the operand and push it to the stack.

If operator:

Pop two nodes from the stack.

Create a new node with the operator.

Assign the first popped node as the right child and the second as the left child.

Push the new node back onto the stack.

After processing all tokens, the stack contains the root of the expression tree.

📌 Step 4: Evaluate the Expression Tree
Define a recursive function:

If the node is a leaf node (operand), return its numeric value.

If the node is an operator, recursively evaluate its left and right children.

Apply the operator to the results and return the final value.

📌 Step 5: Output
Print the evaluated result.

PROGRAM:
```
from binarytree import heap,build,Node
def heaptree(L):
  x=L
  t=build(x)
  for i in t.values:
    print(i,"-->",end='')
  print("\nHeight : ",t.height)
  print("Is max heap? : ",t.is_max_heap)
  print("Is complete tree? : ",t.is_complete)

```

OUTPUT:
![image](https://github.com/user-attachments/assets/f3c1ed08-664f-4384-bf33-d411f59d674e)

RESULT:
Thus, Python program to build and evaluate the given Expression tree was successfully implemented and verified.

