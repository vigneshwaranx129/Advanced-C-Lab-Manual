EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

#include <stdio.h>

#define MAX 5

int stack[MAX] = {10, 20, 30, 40, 50};
int top = 4;

void display()
{
    int i;

    if (top == -1)
    {
        printf("Stack is empty.\n");
        return;
    }

    printf("Stack elements are:\n");

    for (i = top; i >= 0; i--)
    {
        printf("%d\n", stack[i]);
    }
}

int main()
{
    display();
    return 0;
}

Output:

<img width="1642" height="892" alt="image" src="https://github.com/user-attachments/assets/f2603195-3081-4fdd-acaf-9b68dfe892d4" />



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
#include <stdio.h>

#define MAX 5

float stack[MAX];
int top = -1;

void push(float value)
{
    if (top == MAX - 1)
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

int main()
{
    push(10.5);
    push(20.5);
    push(30.5);

    printf("\nStack elements are:\n");

    for (int i = top; i >= 0; i--)
    {
        printf("%.2f\n", stack[i]);
    }

    return 0;
}


Output:

<img width="1338" height="895" alt="image" src="https://github.com/user-attachments/assets/51477f5d-3a12-46ec-aa80-feaf1663749b" />






Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
#include <stdio.h>

#define MAX 5

int queue[MAX] = {10, 20, 30, 40, 50};
int front = 0;
int rear = 4;

void display()
{
    int i;

    if (front == -1 || front > rear)
    {
        printf("Queue is empty.\n");
        return;
    }

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }

    printf("\n");
}

int main()
{
    display();
    return 0;
}


Output:




Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
#include <stdio.h>

#define MAX 5

float queue[MAX];
int front = -1;
int rear = -1;

void enqueue(float value)
{
    if (rear == MAX - 1)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if (front == -1)
            front = 0;

        rear++;
        queue[rear] = value;

        printf("%.2f inserted into queue\n", value);
    }
}

int main()
{
    enqueue(10.5);
    enqueue(20.5);
    enqueue(30.5);

    printf("\nQueue elements are:\n");

    for (int i = front; i <= rear; i++)
    {
        printf("%.2f ", queue[i]);
    }

    printf("\n");

    return 0;
}

Output:
<img width="1292" height="887" alt="image" src="https://github.com/user-attachments/assets/0ce1e9ed-1e51-468f-8fd8-95028c583f4f" />



Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
#include <stdio.h>

#define MAX 5

int queue[MAX] = {10, 20, 30, 40, 50};
int front = 0;
int rear = 4;

void deleteElement()
{
    if (front == -1 || front > rear)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("Deleted element: %d\n", queue[front]);

        front++;

        if (front > rear)
        {
            front = -1;
            rear = -1;
        }
    }
}

int main()
{
    printf("Queue before deletion:\n");

    for (int i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }

    printf("\n\n");

    deleteElement();

    printf("\nQueue after deletion:\n");

    if (front == -1)
    {
        printf("Queue is empty\n");
    }
    else
    {
        for (int i = front; i <= rear; i++)
        {
            printf("%d ", queue[i]);
        }
    }

    printf("\n");

    return 0;
}


Output:
<img width="1330" height="917" alt="image" src="https://github.com/user-attachments/assets/bd24e76e-65e2-4f3b-b920-1b60e6f8dcd4" />




Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
