#include <stdio.h>
#include <conio.h>
#include <math.h>
#include <stdlib.h>

void Bubble(unsigned char *p, unsigned int n)
{
	for(int i=0; i<n-1; i++) 
	{
		bool zamena=false; 
		for(int j=0; j<n-1-i; j++) 
		  if (p[j]>p[j+1]) 
		  {
			  int buf=p[j];
			  p[j]=p[j+1];
			  p[j+1]=buf;
			  zamena=true;
		  }
		if (!zamena) 
			break;
		
	}
}


int main()
{
	unsigned char *p; 
	unsigned int n;
	printf("Enter the number of elements ");
	scanf("%d",&n);
	p=(unsigned char *)malloc(n*sizeof(int)); 
	printf("Value variable");
	for(int j=0;j<n;j++)
	{
		printf("\n");
		scanf("%d",&p[j]);

	}
	for(int i=0; i<n; i++)
	{
		//p[i]=rand() % 1000; 
		printf("%d  ", p[i]);
	}
	printf("\nThe array after sorting:\n");
	Bubble(p, n);
	for(int i=0; i<n; i++)
		printf("%d  ", p[i]);
	system("pause"); 
	return 0;
}




