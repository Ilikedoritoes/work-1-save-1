









#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>
#define N 9

void main()
{
	int num[N], index;
	int middle = N / 3;
	printf("write %d numbers please\n",N);

	for (index = 0; index < N; index++)
	{
		scanf("%d", &num[index]);
	}

	//for (index=0;index;index++)
	//{ 
	//num[index] = num[index] + num[middle * 2];
	//num[middle * 2] = num[0] - num[middle * 2];
	//num[0] = num[0] - num[middle * 2];
	//}

	//num[1] = num[1] + num[middle * 2 + num[1]];
	//num[middle * 2+ num[1]] = num[1] - num[middle * 2 + num[1]];
	//num[1] = num[1] - num[middle * 2 + num[1]];
	
	//num[2] = num[2] + num[middle * 2 + num[2]];
	//num[middle * 2 + num[2]] = num[2] - num[middle * 2 + num[2]];
	//num[2] = num[2] - num[middle * 2 + num[2]];


	//כותב את כול המספרים ברצף בסדר נורמלי
	for (index = 0; index < N; index++)
	{
		printf("%d", num[index]);
	}
	printf("\n");

	//משנה את 123 ל789
	for (index = 0; index < N; index++)
	{

		if (index < middle) 
		{

			//num[index] = num[index + (N - middle)];

			num[index] = num[index] + num[middle * 2];
			num[middle * 2] = num[index] - num[middle * 2];
			num[index] = num[index] - num[middle * 2];

			
		}
	
		printf("%d", num[index]);

	}

	printf("\n");

	//for (index = 0; index < N; index++)
	//{

		//if ((index > 0) && (index < middle))
		//{

			//num[index] = num[index + (N - middle)];
		//}

		//printf("%d", num[index]);
	//}





		system("pause");
}
