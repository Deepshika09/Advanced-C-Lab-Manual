

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
struct Node   
{  
char data[20];  
struct Node *next;  
}*head;  
void display()  
{
    struct Node *t=head;
    if(t==NULL){
        printf("stack is empty");
        
    }
    
    while(t!=NULL){
        printf("%s\n",t->data);
        t=t->next;
    }
    
}
```
Output:

![Screenshot 2025-05-14 230601](https://github.com/user-attachments/assets/650fa107-3f3e-4d29-a8fa-6ff4e30434ce)


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node   
{  
float  data;  
struct Node *next;  
}*head;  
void pop()  
{
    struct Node *t=head;
    if(t==NULL){
        printf("stack is empty");
    }
    else{
        t=head;
        head=t->next;
        free(t);
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/19bd43f2-57aa-4d08-a964-3b5e692f6a71)



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    if(front==NULL){
        printf("queue is empty\n");
    }
    else{
        printf("queue elements:\n");
        while(front!=NULL){
            printf("%c\n",front->data);
            front=front->next;
        }
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/d84679aa-ea3b-48fa-9575-588d4c6856c7)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node* ptr=(struct Node*)malloc(sizeof(struct Node));
    if(ptr==NULL){
        printf("OVERFLOW\n");
    }
    else{
        ptr->data=data;
        if(front==NULL){
            front=ptr;
            rear=ptr;
            front->next=NULL;
            rear->next=NULL;
        }
        else{
            rear->next=ptr;
            rear=ptr;
            rear->next=NULL;
        }
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/6db31a88-7707-4373-b8e3-0fe4b0f0b5d8)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f\n",front->data);
}
```

Output:

![image](https://github.com/user-attachments/assets/6997eca4-3264-4ef2-a22b-7975445d0fe3)



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


