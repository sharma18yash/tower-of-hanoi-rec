#include<stdio.h>
#include<conio.h>
void toh(int n,char,char,char);
void main()
{
  int n;
  printf("enter no. of disks\n");
  scanf("%d",&n);
  toh(n,'A','B','C');
  getch();
}
void toh(int n,char beg,char aux,char end)
{
  if(n>=1)
  {
    toh(n-1,beg,end,aux);
    printf("%c to %c \n" , beg,end);
    toh(n-1,aux,beg,end);
  }
}
