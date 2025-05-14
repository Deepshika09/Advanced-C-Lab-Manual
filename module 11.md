

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max(int,int,int,int);
int main(){
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    int maximum=max(a,b,c,d);
    printf("%d",maximum);
}
int max(int a,int b,int c,int d){
    int m;
    if(a>b&&a>c&&a>d)
    m=a;
    else if(b>c&&b>d)
    m=b;
    else if(c>d)
    m=c;
    else
    m=d;
    return m;
}
```
Output:

![image](https://github.com/user-attachments/assets/44d4f2f7-cdcb-4b6a-8b13-2cbd44365aa4)

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

void calculate_the_maximum(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int a = 1; a < n; a++) {
        for (int b = a + 1; b <= n; b++) {
            int and = a & b;
            int or = a | b;
            int xor = a ^ b;

            if (and < k && and > max_and) max_and = and;
            if (or < k && or > max_or) max_or = or;
            if (xor < k && xor > max_xor) max_xor = xor;
        }
    }

    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
    return 0;
}


```
Output:

![image](https://github.com/user-attachments/assets/e3bdcc7b-8789-4c16-8ccd-3f8a6d192cab)

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include<stdio.h>
#define maxshelves 100
#define maxbooks 100
int main(){
    int shelves[maxshelves][maxbooks];
    int count[maxshelves]= {0};
    int n,q;
    scanf("%d",&n);
    scanf("%d",&q);
    for(int i=0;i<q;i++){
        int type,x,y;
        scanf("%d",&type);
        if(type==1){
        scanf("%d%d",&x,&y);
        shelves[x][count[x]]=y;
        count[x]++;
        }
        else if(type==2){
            scanf("%d%d",&x,&y);
            printf("%d\n",shelves[x][y]);
        }
        else if(type==3){
            scanf("%d",&x);
            printf("%d\n",count[x]);
        }
    }
    return 0;
}

```
Output:

![image](https://github.com/user-attachments/assets/d1147d2b-9156-4a9c-9f27-0363025e4ccf)


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);
    int *arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }

    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }
    printf("%d\n", sum);

    free(arr);

    return 0;
}


```
Output:

![image](https://github.com/user-attachments/assets/ce32718b-add8-4357-8965-bd64c96e9755)

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>

int main() {
    char sentence[1000];
    int i = 0, words = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    while (sentence[i] != '\0') {
        if ((sentence[i] == ' ' || sentence[i] == '\n') && 
            (sentence[i+1] != ' ' && sentence[i+1] != '\n' && sentence[i+1] != '\0')) {
            words++;
        }
        i++;
    }
    if (i > 1)
        words++;
    printf("Number of words: %d\n", words);

    return 0;
}


```
Output:

![Screenshot 2025-05-14 215736](https://github.com/user-attachments/assets/07b2111b-516c-438a-92c9-b98f35c4ac66)


Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
