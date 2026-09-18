## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

## Aim:

To write a C program to search a given element in the given linked list.

## Algorithm:

1. Define the structure for a node in a linked list.
2. Define the search function to find a specific character in the linked list.
3. Initialize the head of the linked list as needed.
4. Call the search function and perform other linked list operations as needed.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *next;
};

void search(struct node *head, char key)
{
    int pos = 1;

    while(head != NULL)
    {
        if(head->data == key)
        {
            printf("Element %c found at position %d", key, pos);
            return;
        }

        head = head->next;
        pos++;
    }

    printf("Element not found");
}

int main()
{
    struct node *head, *second, *third;

    head = (struct node *)malloc(sizeof(struct node));
    second = (struct node *)malloc(sizeof(struct node));
    third = (struct node *)malloc(sizeof(struct node));

    head->data = 'A';
    head->next = second;

    second->data = 'B';
    second->next = third;

    third->data = 'C';
    third->next = NULL;

    search(head, 'B');

    free(head);
    free(second);
    free(third);

    return 0;
}
```

## Output:

<img width="273" height="41" alt="image" src="https://github.com/user-attachments/assets/389bbf22-b37a-45d4-aef6-b73306c6f1a7" />

## Result:

Thus, the program to search a given element in the given linked list is verified successfully.

---

## EXP NO:17 PROGRAM TO INSERT A NODE IN A LINKED LIST.

## Aim:

To write a C program to insert a node in a linked list.

## Algorithm:

1. Define the structure for a node in a linked list.
2. Define the insert function to insert a new node with character data at the end of the linked list.
3. Initialize the head of the linked list as needed.
4. Call the insert function and perform other linked list operations as needed.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *next;
};

struct node *head = NULL;

void insert(char value)
{
    struct node *newnode, *temp;

    newnode = (struct node *)malloc(sizeof(struct node));

    newnode->data = value;
    newnode->next = NULL;

    if(head == NULL)
    {
        head = newnode;
    }
    else
    {
        temp = head;

        while(temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newnode;
    }
}

void display()
{
    struct node *temp;

    temp = head;

    printf("Linked List Elements are:\n");

    while(temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    insert('A');
    insert('B');
    insert('C');

    display();

    return 0;
}
```

## Output:

<img width="254" height="69" alt="image" src="https://github.com/user-attachments/assets/1b36ee17-cddd-48b3-abcf-68daa05408b6" />

## Result:

Thus, the program to insert a node in a linked list is verified successfully.

---

## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

## Aim:

To write a C program to traverse a doubly linked list.

## Algorithm:

1. Initialize a temporary pointer (temp) to the head of the list.
2. Use a while loop to traverse the list until the end (temp == NULL) is reached.
3. Inside the loop, print the data of the current node.
4. Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *prev;
    struct node *next;
};

void traverse(struct node *head)
{
    struct node *temp;

    temp = head;

    printf("Doubly Linked List Elements are:\n");

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct node *head, *second, *third;

    head = (struct node *)malloc(sizeof(struct node));
    second = (struct node *)malloc(sizeof(struct node));
    third = (struct node *)malloc(sizeof(struct node));

    head->data = 10;
    head->prev = NULL;
    head->next = second;

    second->data = 20;
    second->prev = head;
    second->next = third;

    third->data = 30;
    third->prev = second;
    third->next = NULL;

    traverse(head);

    free(head);
    free(second);
    free(third);

    return 0;
}
```

## Output:

<img width="318" height="68" alt="image" src="https://github.com/user-attachments/assets/aba9f447-4ba5-4429-8e3c-4db7b7efe74d" />

## Result:

Thus, the program to traverse a doubly linked list is verified successfully.

---

## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

## Aim:

To write a C program to insert an element in doubly linked list

## Algorithm:

1. Create a new node (newNode) and allocate memory for it.
2. Set the data of the new node to the provided value.
3. If the list is empty, set the new node as the head.
4. If the list is not empty, traverse the list to find the last node.
5. Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *prev;
    struct node *next;
};

struct node *head = NULL;

void insert(int value)
{
    struct node *newNode, *temp;

    newNode = (struct node *)malloc(sizeof(struct node));

    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL)
    {
        newNode->prev = NULL;
        head = newNode;
    }
    else
    {
        temp = head;

        while(temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
        newNode->prev = temp;
    }
}

void display()
{
    struct node *temp;

    temp = head;

    printf("Doubly Linked List Elements are:\n");

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    insert(10);
    insert(20);
    insert(30);

    display();

    return 0;
}
```

## Output:

<img width="305" height="62" alt="image" src="https://github.com/user-attachments/assets/4e004898-ad08-4bd7-82e9-95db388277e9" />

## Result:

Thus, the program to insert an element in doubly linked list is verified successfully.

---

## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim:

To write a C function that deletes a given element from a linked list.

## Algorithm:

1. Check if the Linked List is Empty:

   * If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2. Traverse the Linked List:

   * Start from the head node and iterate through the list to find the node that contains the given element (data).
3. Handle Deletion of the First Node:

   * If the element to be deleted is found in the head node:
   * Update the head of the linked list to point to the next node (i.e., head = head->next).
   * Free the memory allocated to the node to be deleted.
   * Exit the function.
4. Traverse and Delete from the Middle or End:

   * If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
   * When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
   * Free the memory allocated to the node to be deleted.
5. Handle the Case when the Element is Not Found:

   * If the element is not found in any node, print a message indicating the element is not present in the list.
6. End the Function.

## Program:

```c
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head = NULL;

void insert(int value)
{
    struct node *newnode, *temp;

    newnode = (struct node *)malloc(sizeof(struct node));

    newnode->data = value;
    newnode->next = NULL;

    if(head == NULL)
    {
        head = newnode;
    }
    else
    {
        temp = head;

        while(temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newnode;
    }
}

void deleteElement(int key)
{
    struct node *temp, *prev;

    if(head == NULL)
    {
        printf("Linked list is empty\n");
        return;
    }

    temp = head;

    if(temp != NULL && temp->data == key)
    {
        head = temp->next;
        free(temp);

        printf("%d deleted from linked list\n", key);
        return;
    }

    while(temp != NULL && temp->data != key)
    {
        prev = temp;
        temp = temp->next;
    }

    if(temp == NULL)
    {
        printf("Element not found\n");
        return;
    }

    prev->next = temp->next;

    free(temp);

    printf("%d deleted from linked list\n", key);
}

void display()
{
    struct node *temp;

    temp = head;

    printf("Linked List Elements are:\n");

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    printf("\n");
}

int main()
{
    insert(10);
    insert(20);
    insert(30);

    display();

    deleteElement(20);

    display();

    return 0;
}
```

## Output:

<img width="282" height="137" alt="image" src="https://github.com/user-attachments/assets/e31a0d14-ae69-4d6f-bf0e-d905571abbd1" />

## Result:

Thus, the function that deletes a given element from a linked list is verified successfully.
