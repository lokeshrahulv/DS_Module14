# EX.NO : 2(E) Applications of Queue – FCFS
## DATE:
## AIM:
To write a C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm.
## Algorithm
1. Start with process, burst time, and waiting time arrays. 
2. Loop through each process from i = 0 to n-1. 
3. Compute tat[i] = burst_time[i] + wait_time[i]. 
4. End the algorithm. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: ASHWIN KUMAR S
RegisterNumber: 212222240013
*/

```
```c

/*#include <stdio.h>*/
int turnaroundtime( int proc[], int n,int burst_time[], int wait_time[], int tat[]) 
{
    for(int i=0; i<n; i++)
    {
        tat[i] = burst_time[i] + wait_time[i];
    }
    return 0;
}

```

## Output:
![Screenshot 2025-04-25 185957](https://github.com/user-attachments/assets/3941e602-60f8-4f21-9320-bc8083f6f627)


## Result:
Thus, the C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm is implemented successfully.
