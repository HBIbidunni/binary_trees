# ALX Project: C - Binary trees
------------

At the core of this project is __Binary trees__ and its applications.

* __Binary trees__ provide a flexible and efficient structure for organizing and manipulating data, making them valuable in a wide range of applications.

* __Binary trees__ are hierarchical data structures that consist of __nodes__. Each __node__ in a __binary tree__ contains a value and has at most __two child nodes__: a __left child__ and a __right child__. The __left child node__ is smaller than the __parent node__, while the __right child node__ is greater. This property makes __binary trees__ useful for efficient __searching__, __insertion__, and __deletion__ operations.

* To represent a __binary tree__ in __C__, we typically use a `struct` to define the structure of a __node__:

```
struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};

```

In this example, each __node __ contains an integer value (`data`) and two pointers (`left and right`) to its __left__ and __right child nodes__. If a __child node__ is missing, the corresponding pointer is set to `NULL`.

To create a __new node__, we can allocate memory using the __malloc()__ function and initialize its values:

```
struct Node* createNode(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

```
