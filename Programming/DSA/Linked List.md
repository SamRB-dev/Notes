**Prompt**: as a software engineer, Create detail oriented notes on the following concepts with definition, simple explanation, formulas and their representations, use cases, pros and cons and code example in python, C and C++ seperately. The algorithm for the concept should be written in pseudocode for better understanding Linked List and its operations

**Definition:**
A linked list is a linear data structure where elements are stored in nodes. Each node contains a data field and a reference (or pointer) to the next node in the sequence.

**Simple Explanation:**
Think of a linked list as a chain of connected nodes. Each node contains some data and a pointer to the next node in the sequence. Unlike arrays, linked lists don't have to be stored in contiguous memory locations.

**Formulas and Representations:**
- **Node Structure**: Each node typically consists of two parts:
  - Data: Holds the value of the element.
  - Next Pointer: Points to the next node in the sequence.
- **Empty List**: Represented by a null pointer.
- **Traversal**: To traverse the linked list, start from the head node and follow the next pointers until you reach the end (null pointer).
- **Insertion**: Inserting a node involves updating pointers to maintain the correct sequence.
- **Deletion**: Deleting a node involves updating pointers to remove the node from the sequence.

**Use Cases:**
- Dynamic memory allocation: Linked lists can dynamically allocate memory as nodes are added, making them suitable for situations where the size of the data structure is not known in advance.
- Implementing stacks and queues: Linked lists provide an efficient way to implement stack and queue data structures.

**Pros:**
- Dynamic size: Linked lists can grow or shrink dynamically.
- Efficient insertions and deletions: Insertions and deletions can be performed in constant time (O(1)) given a reference to the node.

**Cons:**
- Inefficient access: Random access is not efficient. To access an element at a specific index, you need to traverse the list from the beginning, which takes linear time (O(n)).
- Extra memory overhead: Linked lists require extra memory for storing pointers.

**Pseudo code for Operations:**
- **Insertion at the beginning:**
  ```
  InsertAtBeginning(data):
      newNode = CreateNode(data)
      newNode.next = head
      head = newNode
  ```

- **Insertion at the end:**
  ```
  InsertAtEnd(data):
      newNode = CreateNode(data)
      if head is null:
          head = newNode
      else:
          currentNode = head
          while currentNode.next is not null:
              currentNode = currentNode.next
          currentNode.next = newNode
  ```

- **Deletion by value:**
  ```
  DeleteByValue(value):
      if head is null:
          return
      if head.data == value:
          head = head.next
          return
      currentNode = head
      while currentNode.next is not null:
          if currentNode.next.data == value:
              currentNode.next = currentNode.next.next
              return
          currentNode = currentNode.next
  ```

**Code Example in Python:**
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert_at_beginning(self, data):
        newNode = Node(data)
        newNode.next = self.head
        self.head = newNode

    def insert_at_end(self, data):
        newNode = Node(data)
        if self.head is None:
            self.head = newNode
        else:
            currentNode = self.head
            while currentNode.next is not None:
                currentNode = currentNode.next
            currentNode.next = newNode

    def delete_by_value(self, value):
        if self.head is None:
            return
        if self.head.data == value:
            self.head = self.head.next
            return
        currentNode = self.head
        while currentNode.next is not None:
            if currentNode.next.data == value:
                currentNode.next = currentNode.next.next
                return
            currentNode = currentNode.next
```

**Code Example in C:**
```c
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

void insertAtBeginning(struct Node** headRef, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = *headRef;
    *headRef = newNode;
}

void insertAtEnd(struct Node** headRef, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    struct Node* last = *headRef;
    newNode->data = data;
    newNode->next = NULL;
    if (*headRef == NULL) {
        *headRef = newNode;
        return;
    }
    while (last->next != NULL)
        last = last->next;
    last->next = newNode;
    return;
}

void deleteByValue(struct Node** headRef, int value) {
    struct Node* temp = *headRef;
    struct Node* prev = NULL;
    if (temp != NULL && temp->data == value) {
        *headRef = temp->next;
        free(temp);
        return;
    }
    while (temp != NULL && temp->data != value) {
        prev = temp;
        temp = temp->next;
    }
    if (temp == NULL)
        return;
    prev->next = temp->next;
    free(temp);
}

int main() {
    struct Node* head = NULL;
    insertAtEnd(&head, 1);
    insertAtEnd(&head, 2);
    insertAtEnd(&head, 3);
    insertAtEnd(&head, 4);
    printf("Linked list: ");
    struct Node* temp = head;
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    deleteByValue(&head, 3);
    printf("\nAfter deleting 3: ");
    temp = head;
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    return 0;
}
```

**Code Example in C++:**
```cpp
#include <iostream>

using namespace std;

struct Node {
    int data;
    Node* next;
    Node(int data) : data(data), next(nullptr) {}
};

class LinkedList {
private:
    Node* head;
public:
    LinkedList() : head(nullptr) {}

    void insertAtBeginning(int data) {
        Node* newNode = new Node(data);
        newNode->next = head;
        head = newNode;
    }

    void insertAtEnd(int data) {
        Node* newNode = new Node(data);
        if (head == nullptr) {
            head = newNode;
            return;
        }
        Node* last = head;
        while (last->next !=

 nullptr)
            last = last->next;
        last->next = newNode;
    }

    void deleteByValue(int value) {
        Node* temp = head;
        Node* prev = nullptr;
        if (temp != nullptr && temp->data == value) {
            head = temp->next;
            delete temp;
            return;
        }
        while (temp != nullptr && temp->data != value) {
            prev = temp;
            temp = temp->next;
        }
        if (temp == nullptr)
            return;
        prev->next = temp->next;
        delete temp;
    }

    void display() {
        Node* temp = head;
        while (temp != nullptr) {
            cout << temp->data << " ";
            temp = temp->next;
        }
        cout << endl;
    }
};

int main() {
    LinkedList ll;
    ll.insertAtEnd(1);
    ll.insertAtEnd(2);
    ll.insertAtEnd(3);
    ll.insertAtEnd(4);
    cout << "Linked list: ";
    ll.display();
    ll.deleteByValue(3);
    cout << "After deleting 3: ";
    ll.display();
    return 0;
}
```

These examples demonstrate the implementation of a linked list and its operations in Python, C, and C++.