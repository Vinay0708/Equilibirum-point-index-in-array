# Equilibirum-point-index-in-array
 #include<stdio.h>
int equilibrium(int arr[], int n)
{
    int i, j;
    int leftsum, sum;
    for (i = 0; i < n; ++i)
    {      
 
        leftsum = 0;
        for (j = 0; j < i; j++)
            leftsum =leftsum+arr[j];
        sum = 0;
        for (j = i + 1; j < n; j++)
            sum = sum+arr[j];
        if (leftsum == sum)
            return i;
    }
    return -1;
}
int main()
{
    int arr[] = { -3,2,4,-5,1,3 };
    int n = sizeof(arr) / sizeof(arr[0]);
    printf("%d", equilibrium(arr, n));
    return 0;
}
