# Experiment 9(c): Expression Tree – Inorder and Postorder Traversal

## Aim
To write a Python program to build the following expression tree and print the inorder and postorder traversal.


---

## Algorithm

1. Begin the program.
2. Import the necessary modules (`build`, `Node`) from the `binarytree` package.
3. Define a list `x` representing the binary tree in pre-order format.
4. Use the `build()` function to construct the expression tree from the list.
5. Print the inorder traversal of the expression tree using `.inorder`.
6. Print the postorder traversal of the expression tree using `.postorder`.
7. End the program.

---

## Program

```
from binarytree import build

l=["*","+","-",9,3,8,4]
bt=build(l)
print(bt.inorder)
print(bt.postorder)
```

## OUTPUT
![Screenshot 2025-05-05 010329](https://github.com/user-attachments/assets/5849de8f-be57-4566-82db-4f6e5379dbc9)

## RESULT
Thus the program succesffuly completed the Build an Expression Tree and Print Inorder and Postorder Traversals and executrd successfully.
