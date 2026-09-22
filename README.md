# Ex6 Dequeue Elements from Circular Queue
## DATE: 
## AIM:
To write a C program to delete three elements from the filled circular queue.

## Algorithm
```
1. Start
2.Define a queue with a fixed size SIZE and initialize front and rear pointers.
3.Define the deQueue() function to remove and return an element from the front of the queue.
4.Check if the queue is empty using isEmpty(); if empty, print an error message.
5.If the queue has one element, reset both front and rear to -1.
6.If the queue has more than one element, update front to the next index using modulo operation ((front + 1) % SIZE).
7.Return the removed element from the front of the queue.
8.End
```
## Program:
```
/*
Program to delete three elements from the filled circular queue
Developed by: kirthick roshan j
RegisterNumber: 212223040097

#include <stdio.h> 
#define SIZE 5 
int items[SIZE]; 
int front = -1, rear = -1; 
*/ 
int deQueue() 
{ 
int element; 
element=items[front]; 
if(isEmpty()) 
{ 
printf("Queue is Empty!!"); 
} 
else 
{ 
if(front==rear) 
{ 
front=-1; 
rear=-1; 
} 
  
  
else 
{ 
front=(front+1)%SIZE; 
} 
} 
return element; 
}  
*/
```

## Output:

![image](https://github.com/user-attachments/assets/2e8f09af-ef23-475c-b22a-16ec23633893)

# Ex7 Priority Queue
## AIM:
To formulate the C code to display the elements of the priority queue after insertion and deletion operation.

## Algorithm
```
1. Start
2.Define a function printArray() that takes an array and its size as parameters.
3.Loop through the array from index 0 to size-1.
4.Print each element of the array during the loop.
5.After printing all elements, print a newline for formatting.
6.End  
```
## Program:
```
/*
Program to o display the elements of the priority queue after insertion and deletion operation
Developed by: kirthick roshan j
RegisterNumber: 212223040097

/*#include <stdio.h> 
int size = 0; 
*/ 
void printArray(int array[], int size) 
{ 
int i; 
for(i=0;i<size;i++) 
{ 
printf("%d ",array[i]); 
} 
printf("\n"); 
}
*/
```

## Output:

![image](https://github.com/user-attachments/assets/c37940ff-0e87-464f-af8a-d46cdf1cf49b)


## Result:
Thus, the C program to display the elements of the priority queue after insertion and deletion operation is implemented successfully


# Ex8 Deque
## AIM:
To write a C function to count the number of elements present in the deque.

## Algorithm
```
1.Start
2.Define a function count() that takes an array arr as input.
3.Initialize a counter c to track the number of non-zero elements.
4.Loop through the array from index 0 to MAX-1.
5.For each element, check if it's non-zero.
6.If the element is non-zero, increment the counter c.
7.Return the final count of non-zero elements in the array.
8.End
``` 

## Program:
```
/*
Program to count the number of elements present in the deque
Developed by: kirthick roshan j
RegisterNumber: 212223040097

#include <stdio.h> 
#define MAX 10 
void addFront(int *, int, int *, int *); 
void addRear(int *, int, int *, int *); 
int delFront(int *, int *, int *); 
int delRear(int *, int *, int *); 
void display(int *); 
int count(int *); 
*/ 
int count(int *arr) { 
int c = 0, i; 
for(i=0;i<MAX;i++) 
{ 
if(arr[i]!=0) 
{ 
c=c+1; 
} 
} 
return c; 
} 
*/
```

## Output:

![image](https://github.com/user-attachments/assets/a0d9c4d5-e12b-49a1-abb6-15dbcc9a460a)


## Result:
Thus, the C code to count the number of elements present in the deque is implemented successfully.


# Ex9 Applications of Queue - SJF
## AIM:
To incorporate the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
## Algorithm
```
1. start
2. Read the number of processes n and their burst times into the array bt[]. 
3. Assign process numbers to array p[] (from 1 to n). 
4. Sort the processes based on burst time using selection sort, updating both bt[] and p[] arrays. 
5. Calculate the waiting time wt[] for each process by summing burst times of previous 
processes. 
6. Calculate the turnaround time tat[] as the sum of burst time and waiting time for each 
process. 
7. Compute and print the average waiting time and average turnaround time. 
8. End
```
## Program:
```
/*
Program to find the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
Developed by: kirthick roshan j
RegisterNumber: 212223040097

#include<stdio.h> 
int main() 
{ 
int bt[20],p[20],wt[20],tat[20],i,j,n,total=0,pos,temp; 
float avg_wt,avg_tat; 
scanf("%d",&n); 
for(i=0;i<n;i++) 
{ 
scanf("%d",&bt[i]); 
p[i]=i+1; 
} 
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
 
wt[0]=0; 
for(i=1;i<n;i++) 
{ 
wt[i]=0; 
for(j=0;j<i;j++) 
wt[i]+=bt[j]; 
total+=wt[i]; 
} 
 
avg_wt=(float)total/n; 
total=0; 
printf("Process Burst Time Waiting Time Turnaround Time\n"); 
for(i=0;i<n;i++) 
{ 
tat[i]=bt[i]+wt[i]; //calculate turnaround time 
total+=tat[i]; 
//printf("\n"); 
printf("p%d %d %d %d\n",p[i],bt[i],wt[i],tat[i]); 
} 
 
avg_tat=(float)total/n; //average turnaround time 
// printf("\n"); 
printf("Average Waiting Time=%f\n",avg_wt); 
// printf("\n"); 
printf("Average Turnaround Time=%f\n",avg_tat); 
return 0; 
} 

*/
```

## Output:

![image](https://github.com/user-attachments/assets/f0b51994-aa40-445f-b57a-d11f0a2a9fe4)


## Result:
Thus, the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm is implemented successfully.


# Ex10 Applications of Queue – FCFS
## AIM:
To write a C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm.
## Algorithm
```
1. Start with process, burst time, and waiting time arrays. 
2. Loop through each process from i = 0 to n-1. 
3. Compute tat[i] = burst_time[i] + wait_time[i]. 
4. End the algorithm.
```

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: kirthick roshan j
RegisterNumber: 212223040097

int turnaroundtime( int proc[], int n,int burst_time[], int wait_time[], int tat[]) { 
   // calculating turnaround time by adding 
   // burst_time[i] + wait_time[i] 
   int i; 
   for ( i = 0; i < n ; i++) 
   tat[i] = burst_time[i] + wait_time[i]; 
   return 0; 
} 
*/
```

## Output:

![image](https://github.com/user-attachments/assets/760a67f0-8e10-4e10-9cf3-7ebf72f87811)


## Result:
Thus, the C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm is implemented successfully.

## Result:
Thus, the C program to delete three elements from the filled circular queue is implemented successfully.
