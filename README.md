#include<stdio.h>
#define num 10

int main(void)
{
	int i;
	int fib[num]={1, 1};
	
	for(i=2; i<num; i++)
		fib[i]=fib[i-1]+fib[i-2];
	
	for(i=0; i<num; i++) {
		printf("%6d", fib[i]);
		if(fib[i]%5==0)
			printf("\n");
	}
		
	return 0;
#include<stdio.h>
#define num 10

int main(void)
{
	int i;
	int fib[num]={1, 1};
	
	for(i=2; i<num; i++)
		fib[i]=fib[i-1]+fib[i-2];
	
	for(i=0; i<num; i++) {
		printf("%6d", fib[i]);
		if(fib[i]%5==0)
			printf("\n");
	}
		
	return 0;
}
