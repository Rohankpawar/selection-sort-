# selection-sort-
code of selection sort 
#include <stdio.h>

int main() {
    int i,j,n,temp,s,arr[10];
    //Taking array size
    printf("Enter the size of an array: \n");
    scanf("%d",&n);
    
    //Taking array elements
    printf("Enter the array elements: \n");
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    
    //printing array elements
    for(i=0;i<n;i++)
    {
        printf("%d \t",arr[i]);
    }
    printf("\n");
    // Algorithm 
    for(i=0;i<n-1;i++)
    {
        s=i;
        for(j=i+1;j<n;j++)
        {
           if(arr[j]<arr[s])
           {
               s=j;
           }
        }
           if(i!=s)
           {
               // Swap two number by third variable temp  
               temp=arr[i];
               arr[i]=arr[s];
               arr[s]=temp;
           }
    }
    printf("The sorted array in ascending \n");
    for(i=0;i<n;i++)
    {
       printf("%d \t",arr[i]); 
    }
    printf("\n");
    printf("The sorted array in descending \n");
    
    for(i=n-1;i>=0;i--)
    {
        printf("%d \t",arr[i]);
    }
    return 0;
}
