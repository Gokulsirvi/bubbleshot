#include <stdio.h>
int main()
{
    int arr[] = {4, 5, 6, 3, 2, 1};
    for (int i = 0; i < 6; i++)
    {
        printf("element %d = %d\n", i, arr[i]);
        // scanf("%d \n",& arr[i]);
    }
    for (int i = 0; i < 6; i++)
    {
        for (int j = 1; j < 6 - i; j++)
        {
            if (arr[j] < arr[j - 1])
            {
                int temp = arr[j-1];
                arr[j - 1] = arr[j];
                arr[j] = temp;
            }
        }
    }
    printf("after sorting array \n [");
    for (int i = 0; i < 6; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("]");
    return 0;
}
