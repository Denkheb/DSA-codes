// Tower of hanoi with recursion
#include<stdio.h>

void towerofhanoi(int n, char from_tower, char to_tower, char aux_tower)
{
	if(n==1)
	{
		printf("\n shift disk 1 from tower %c to tower %c", from_tower, to_tower);
		return;
	}
	towerofhanoi(n-1, from_tower, aux_tower, to_tower);
	printf("\n shift disk %d from tower %c to tower %c", n,from_tower, to_tower);
	towerofhanoi(n-1, aux_tower, to_tower, from_tower);
}

int main()
{
	int n;
	printf("enter the number of disks : ");
	scanf("%d",&n);
	
	towerofhanoi(n,'A', 'C','B');
	return 0;
}
