#include<stdio.h>
 
int doSum(int);
int main()
{
    int num,sum;
    printf("Enter a Number  : ");
    scanf("%d",&num);
 
    sum = doSum(num);
 
    printf("Sum of Digits :  %d",sum);
    return 0;
}
 
int doSum(int num)
{
 
    static int sum =0,r;
 
    if(num!=0)
    {
        r=num%10;
        sum=sum+r;
        doSum(num/10);
    }
 
    return sum;
}
