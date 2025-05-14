## NAME : MANASA DEVI A.T
## REG NO : 212224110036

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
#include <stdio.h>
int findGreatest(int num1, int num2, int num3) {
    if (num1 >= num2 && num1 >= num3) {
        return num1;  
    } else if (num2 >= num1 && num2 >= num3) {
        return num2;  
    } else {
        return num3;  
    }
}
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    int greatest = findGreatest(a, b, c);
    printf("The greatest number is: %d\n", greatest);
    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/016ff3fc-34da-4462-a173-9b8c37f41a07)

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
#include<stdio.h>
void calc(int n,int k)
{
    int max_and=0,max_or=0,max_not=0;
    for(int a=1;a<n;a++)
    {
        for(int b=a+1;b<=n;b++)
        {
            int and_res=a&b;
            int or_res=a|b;
            int not_res=a^b;
            
            if(and_res<k && and_res>max_and)
               max_and=and_res;
             if(or_res<k && or_res>max_or)
               max_or=or_res;
            if(not_res<k && not_res>max_not)
               max_not=not_res;
        }
    }
    printf("%d\n%d\n%d\n",max_and,max_or,max_not);
}
int main()
{
    int n,k;
    scanf("%d%d",&n,&k);
    calc(n,k);
}
```
Output:

![image](https://github.com/user-attachments/assets/728fa003-40f4-4255-953f-f67574875e0a)

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
#include <stdio.h>
int findGreatest(int num1, int num2, int num3) {
    if (num1 >= num2 && num1 >= num3) {
        return num1;
    } else if (num2 >= num1 && num2 >= num3) {
        return num2;
    } else {
        return num3;
    }
}
int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}
int add(int a, int b) {
    return a + b;
}
int subtract(int a, int b) {
    return a - b;
}

int main() {
    int choice, num1, num2, num3;

    while (1) {
        printf("\nMenu:\n");
        printf("1. Find the greatest number\n");
        printf("2. Calculate factorial\n");
        printf("3. Add two numbers\n");
        printf("4. Subtract two numbers\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter three numbers: ");
                scanf("%d %d %d", &num1, &num2, &num3);
                printf("The greatest number is: %d\n", findGreatest(num1, num2, num3));
                break;

            case 2:
                printf("Enter a number to calculate factorial: ");
                scanf("%d", &num1);
                printf("The factorial of %d is: %d\n", num1, factorial(num1));
                break;

            case 3:
                printf("Enter two numbers to add: ");
                scanf("%d %d", &num1, &num2);
                printf("The sum is: %d\n", add(num1, num2));
                break;

            case 4:
                printf("Enter two numbers to subtract: ");
                scanf("%d %d", &num1, &num2);
                printf("The result is: %d\n", subtract(num1, num2));
                break;

            case 5:
                printf("Exiting program...\n");
                return 0;

            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/eb2168e6-0822-457e-a63a-fb1b450e2e3b)

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
#include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int arr[100];
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++)
    {
        sum=sum+arr[i];
    }
    printf("%d",sum);
}
```
Output:

![image](https://github.com/user-attachments/assets/37496ad6-0997-4d75-b1c3-ddee9dd01ef0)

Result:
Thus, the program prints the sum of the integers in the array is verified successfully.

EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE
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
#include <ctype.h>
int countWords(char str[]) {
    int count = 0;
    int inWord = 0;  
    for (int i = 0; str[i] != '\0'; i++) {
        if (isspace(str[i])) {
            inWord = 0;
        } else {
            if (inWord == 0) {
                count++;  // Found a new word
                inWord = 1;
            }
        }
    }
    return count;
}
int main() {
    char sentence[1000];
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);  // Using fgets to allow spaces
    int wordCount = countWords(sentence);
    printf("The number of words in the sentence is: %d\n", wordCount);
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/ac1065ea-2b7c-4ce3-b774-80c542888553)

Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
