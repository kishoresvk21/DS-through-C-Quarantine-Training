							:::PROGRAMS:::
1,2,3:printing factors,no of factors,sum of factors

#include<stdio.h>
#include<conio.h>
void main()
{
	int n,sum=0,count=0,i;
	scanf("%d",&n);
	printf("The factors are:");
	for(i=1;i<=n;i++)
	{
		if(n%i==0)
		{
			count++;
			printf("%d\n",i);
			sum+=i;
		}
	}
	printf("no of factors are:%d\n",count);
	printf("sum of factors are:%d\n",sum);
}

4.PERFECT NUMBER:

#include<stdio.h>
#include<conio.h>
void main()
{
	int n,i,sum=0;
	scanf("%d",&n);
	for(i=1;i<n;i++)
	{
		if(n%i==0)
		{
			sum+=i;
		}
	}
	if(sum==n)
	{
		printf("PERFECT NUMBER");
	}
	else
	{
		printf("NOT A PERFECT NUMBER");
	}
}

5.AMICABLE NUMBER:

#include<stdio.h>
#include<conio.h>
void main()
{
	int i,val1,val2;
	scanf("%d %d",&val1,&val2);
	if(factorssum(val1)==val2 &&factorssum(val2)==val1)
	{
		printf("These two are amicable");
	}
	else
	{
		printf("not amicable");
	}
}
int factorssum(int val)
{
	int i,sum=0;
	for(i=1;i<val;i++)
	{
		if(val%i==0)
		{
			sum+=i;
		}
	}
	return sum;
}

6.PRIME NUMBERS:

#include<stdio.h>
#include<conio.h>
void main()
{
	int n,i,count=0;
	scanf("%d",&n);
	for(i=1;i<=n;i++)
	{
		if(n%i==0)
		{
			count++;
		}
	}
	if(count>2)
	{
		printf("NOT A PRIME NUMBER");
	}
	else
	{
		printf("PRIME NUMBER");
	}
}

7.PRIME FACTORS:
#include<stdio.h>
#include<conio.h>
void main()
{
	int i,j,n,isprime;
	int res[40],count=0;
	scanf("%d",&n);
	printf("Prime factors are: ");
	for(i=2;i<=n;i++)
	{
		if(n%i==0)
		{
			isprime=1;
			for(j=2;j<=i/2;j++)
			{
				if(i%j==0)
				{
					isprime=0;
					break;
				}
			}
			if(isprime==1)
			{
				res[count]=i;
				count++;
			}
		}
	}
	for(i=0;i<count;i++)
	{
		printf("%d\n",res[i]);
	}
	printf("LARGEST PRIME FACTOR IS :%d\n",res[count-1]);
}

8.GCD:

#include<stdio.h>
#include<conio.h>
void main()
{
	int a,b,k;
	scanf("%d %d",&a,&b);
	k=gcd(a,b);
	printf("GCD is:%d",k);
}
int gcd(int a,int b)
{
	if(a==0)
	{
		return b;
	}
	else if(b==0)
	{
		return a;
	}
	else
	{
		gcd(b,a%b);
	}
}

EXTRA PROGRAMS:

1.COMMON FACTORS 
2.COUNT OF COMMON FACTORS
3.COUNT OF ODD COMMON FACTORS
4.SUM OF FACTORIAL OF COMMON FACTORS:


#include<stdio.h>
void main()
{
	int n,a[10],res[20],count=0,s,i,j,ko=0,f[20],oddcount=0,sum=0;
	printf("Enter no of inputs u need:");
	scanf("%d",&n);
	printf("Enter %d values:",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
	}
	for(i=1;i<=a[0];i++)
	{
	    if(a[0]%i==0)
	    {
	        res[count]=i;
	        count++;
	    }
	}
	for(i=0;i<=count;i++)
	{
	    s=0;
	    for(j=0;j<n;j++)
	    {
	        if(a[i]%res[j]==0)
	        {
	            s=1;
	        }
	    }
	    if(s==1)
	    {
	        f[ko]=res[i];
	        ko++;
	        sum+=fact(res[i]);
	        if(res[i]%2!=0)
	        {
	        	oddcount++;
			}
	    }
	}
	for(i=0;i<ko-1;i++)
	{
		printf("%d\n",f[i]);
	}
	printf("The count of common factors are: %d\n",ko-1);
	printf("The count of odd common factors are:%d\n",oddcount);
	printf("The sum of factorial of common factors:%d\n",sum);
}
int fact(int val)
{
	if(val==0)
	{
		return 1;
	}
	else
	{
		return val*fact(val-1);
	}
}



 							:::APTITUDE:::
1.1/5
2.28/143
3.3/51
4.7/22
5.1/8
6.8/15
7.17/40
8.0.9
9.56/126
10.9/13