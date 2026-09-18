## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:

To write a C program to display stack elements using an array.

## Algorithm:

1. Include Necessary Header Files
2. Declare Global Variables
3. Define the Display Function
4. Main Function (or Other Relevant Code)
5. Initialize the stack and top as needed.
6. Perform stack operations (push, pop, etc.).
7. Use the display function to visualize the stack's contents

## Program:

```c
#include <stdio.h>

#define MAX 5

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%d pushed into stack\n", value);
    }
}

void pop()
{
    if(top == -1)
    {
        printf("Stack Underflow\n");
    }
    else
    {
        printf("%d popped from stack\n", stack[top]);
        top--;
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is empty\n");
    }
    else
    {
        printf("Stack elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    pop();

    display();

    return 0;
}
```

## Output:

<img width="286" height="272" alt="image" src="https://github.com/user-attachments/assets/425cb28e-00f4-49d5-8c04-65e9ca39ae89" />

## Result:

Thus, the program to display stack elements using an array is verified successfully.

---

## EXP NO:12 PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

## Aim:

To create a C program to push the given element in to a stack using array.

## Algorithm:

1. Declare global variables for the stack size, top index, and the stack itself.
2. Define the push function to add a floating-point number to the stack.
3. Initialize the stack size, top index, and the stack itself.
4. Call the push function as needed.

## Program:

```c
#include <stdio.h>

#define MAX 5

float stack[MAX];
int top = -1;

void push(float value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;

        printf("%.2f pushed into stack\n", value);
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is empty\n");
    }
    else
    {
        printf("Stack elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%.2f\n", stack[i]);
        }
    }
}

int main()
{
    push(10.5);
    push(20.8);
    push(30.2);

    display();

    return 0;
}
```

## Output:

<img width="246" height="174" alt="image" src="https://github.com/user-attachments/assets/3ffa6765-3103-4e37-856a-f75de22f6466" />

## Result:

Thus, the program to push the given element in to a stack using array is verified successfully.

---

## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

## Aim:

To write a C program to display queue elements using array

## Algorithm:

1. Declare global variables for the queue, rear, front, and iteration.
2. Define the display function to print the elements of the queue.
3. Initialize the queue, rear, and front as needed.
4. Call the display function and perform other queue operations as needed.

## Program:

```c
#include <stdio.h>

#define MAX 5

int queue[MAX];
int front = -1, rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if(front == -1)
            front = 0;

        rear++;
        queue[rear] = value;

        printf("%d inserted into queue\n", value);
    }
}

void display()
{
    int i;

    if(front == -1 || front > rear)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++)
        {
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

## Output:

<img width="230" height="178" alt="image" src="https://github.com/user-attachments/assets/53d8be40-30d5-4908-add6-85c0013663d2" />

## Result:

Thus, the program to display queue elements using array is verified successfully.

---

## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

## Aim:

To write a C program to insert elements in queue using array.

## Algorithm:

1. Declare global variables for the size, rear, front, and the queue itself.
2. Define the enqueue function to add a float to the queue.
3. Initialize the rear, front, and size of the queue as needed.
4. Call the enqueue function as needed.

## Program:

```c
#include <stdio.h>

#define SIZE 5

float queue[SIZE];
int front = -1, rear = -1;

void enqueue(float value)
{
    if(rear == SIZE - 1)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if(front == -1)
            front = 0;

        rear++;
        queue[rear] = value;

        printf("%.2f inserted into queue\n", value);
    }
}

void display()
{
    int i;

    if(front == -1)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++)
        {
            printf("%.2f\n", queue[i]);
        }
    }
}

int main()
{
    enqueue(10.5);
    enqueue(20.8);
    enqueue(30.2);

    display();

    return 0;
}
```

## Output:

<img width="273" height="185" alt="image" src="https://github.com/user-attachments/assets/874cefe7-02ee-41c1-8720-a4c9cd91a527" />

## Result:

Thus, the program to insert elements in queue using array is verified successfully.

---

## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

1. Check if the Queue is Empty

   * If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2. Delete the Front Element

   * If the queue is not empty, the element at the front index is deleted.
   * Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3. Check if the Queue Becomes Empty After Deletion:

   * After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4. End the Function.

## Program:

```c
#include <stdio.h>

#define SIZE 5

int queue[SIZE];
int front = -1, rear = -1;

void enqueue(int value)
{
    if(rear == SIZE - 1)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if(front == -1)
            front = 0;

        rear++;
        queue[rear] = value;
    }
}

void dequeue()
{
    if(front == -1)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("%d deleted from queue\n", queue[front]);

        front++;

        if(front > rear)
        {
            front = rear = -1;
        }
    }
}

void display()
{
    int i;

    if(front == -1)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++)
        {
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    dequeue();

    display();

    return 0;
}
```

## Output:

<img width="252" height="210" alt="image" src="https://github.com/user-attachments/assets/d2a5a38f-b3d8-414f-987f-f6eccbe3c009" />

## Result:

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
