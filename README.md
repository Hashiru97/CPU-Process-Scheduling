# CPU-Process-Scheduling
#include<stdio.h>
#include<stdlib.h>
main()
{
int BT[15]={0},TAT[15]={0},WT[15]={0},n,i;
system("clear");
printf("\n Enter the no of Processes-\n");
scanf("%d",&n);
for(i=0;i<n;i++)
{
printf("\nEnter the Burst Time of P[%d] - ",i);
scanf("%d",&BT[i]);
}
for(i=1;i<n;i++)
{
WT[i]=WT[i-1]+BT[i-1];
}
for(i=0;i<n;i++)
{
TAT[i]+=WT[i]+BT[i];
}
printf("\n TAT and WT of Processes using FCFS are-\n");
for(i=0;i<n;i++)
{
printf("\nP[%d]\tWT=%d\tTAT=%d\n",i,WT[i],TAT[i]);
}
}
