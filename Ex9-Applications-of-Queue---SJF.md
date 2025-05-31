# EX.NO : 2(D) Applications of Queue - SJF
## DATE:
## AIM:
To incorporate the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
## Algorithm
1. Start 
2. Read the number of processes n and their burst times into the array bt[]. 
3. Assign process numbers to array p[] (from 1 to n). 
4. Sort the processes based on burst time using selection sort, updating both bt[] and p[] arrays. 
5. Calculate the waiting time wt[] for each process by summing burst times of previous processes. 
6. Calculate the turnaround time tat[] as the sum of burst time and waiting time for each process. 
7. Compute and print the average waiting time and average turnaround time. 
8. End
 

## Program:
```
/*
Program to find the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
Developed by: LOKESH RAHUL V V
RegisterNumber: 212222100024
*/
```
```c

#include<stdio.h>
 
int main()
{
    int bt[20],p[20],wt[20],tat[20],i,j,n,total=0, temp, pos;
    float avg_wt,avg_tat;

    //printf("Enter number of process:");
    scanf("%d",&n);
 
    // printf("\nEnter Burst Time:\n");
    for(i=0;i<n;i++)
    {
        //  printf("p%d:",i+1);
        scanf("%d",&bt[i]);
        p[i]=i+1;           
    }
 
    //sorting burst time in ascending order using selection sort
    for(i=0;i<n;i++)
    {
        pos=i;
        for(j=i+1;j<n;j++)
        {
            if(bt[j]<bt[pos])
                pos=j;
        }
 
        temp=bt[i];
        bt[i]=bt[pos];
        bt[pos]=temp;
 
        temp=p[i];
        p[i]=p[pos];
        p[pos]=temp;
    }
 
    wt[0]=0;            //waiting time for first process will be zero
 
    for(int i=1; i<n; i++)
    {
        wt[i] = wt[i-1]+bt[i-1];
        avg_wt += wt[i];
    }
    avg_wt = avg_wt/n;
    
    total = 0;
    printf("Process    Burst Time    Waiting Time  Turnaround Time\n");
    for(i=0;i<n;i++)
    {
        tat[i]=bt[i]+wt[i];     //calculate turnaround time
        total+=tat[i];
        //printf("\n");
        printf("p%d          %d               %d             %d\n",p[i],bt[i],wt[i],tat[i]);
    }
 
    avg_tat=(float)total/n;     //average turnaround time
    // printf("\n");
    printf("Average Waiting Time=%f\n",avg_wt);
    //  printf("\n");
    printf("Average Turnaround Time=%f\n",avg_tat);
    return 0;
}

```

## Output:
![image](https://github.com/user-attachments/assets/0c2c8fc1-c00c-448b-b5ad-f445cac32190)



## Result:
Thus, the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm is implemented successfully.
