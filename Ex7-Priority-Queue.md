# EX.NO : 2(B) Priority Queue
## DATE:
## AIM:
To formulate the C code to display the elements of the priority queue after insertion and deletion operation.

## Algorithm
1. Start 
2. Define a function printArray() that takes an array and its size as parameters. 
3. Loop through the array from index 0 to size-1. 
4. Print each element of the array during the loop. 
5. After printing all elements, print a newline for formatting. 
6. End    

## Program:
```
/*
Program to display the elements of the priority queue after insertion and deletion operation
Developed by: LOKESH RAHUL V V
RegisterNumber: 212222100024 
*/

```
```c

/*#include <stdio.h>
int size = 0;
*/
void printArray(int array[], int size) {
  int i;
  if(size == 0)
  {
      printf("Heap is empty");
  }
  else
  {
    for(i=0; i<size; i++)
    {
      printf("%d ", array[i]);
    }
  }
  
}

```
## Output:
![image](https://github.com/user-attachments/assets/367f4108-11e7-4413-a568-468ac097cb4e)



## Result:
Thus, the C program to display the elements of the priority queue after insertion and deletion operation is implemented successfully
