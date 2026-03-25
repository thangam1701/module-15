# Experiment 9(e): Expression Tree Evaluation

## Aim
To write a Python program to build and evaluate the given expression tree.

---

## Algorithm

1. Start the program.
2. Create nodes for operators and operands.
3. Build the expression tree by connecting the nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it as a float.
   - Else, recursively evaluate the left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. End the program.

---

## Program

```
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
 

def isLeaf(node):
    return node.left is None and node.right is None
 
def process(op, x, y):
    if op == '+':
        return x + y
    if op == '-':
        return x - y
    if op == '*':
        return x * y
    if op == '/':
        return x / y
 
def evaluate(root):

    if root is None:
        return 0
  
    if isLeaf(root):
        return float(root.val)
    
    x = evaluate(root.left)
    y = evaluate(root.right)
    return (process(root.val, x, y))
    


root = Node('/')
root.left = Node('*')
root.right = Node('+')
root.left.left = Node('+')
root.left.right = Node(4)
root.right.left = Node('-')
root.right.right = Node(2)
root.left.left.left = Node(3)
root.left.left.right = Node(1)
root.right.left.left = Node(9)
root.right.left.right = Node(5)
print('The value of the expression tree is',evaluate(root))

```

## OUTPUT
![Screenshot 2025-05-05 005758](https://github.com/user-attachments/assets/797eb3fa-b809-4c88-abe3-9f7bcf3c2faf)


## RESULT
Thus The result of the expression tree evaluation is the computed value derived from traversing the tree and applying the operations based on the operator nodes and operand values at the leaf nodes.
