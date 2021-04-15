include<stdio.h>
#include<string.h>

int main()
{
    int row,col,k,n = 0;
    char arr[50];
    scanf("%s",arr);
    int len = strlen(arr);
    int middle =len / 2;
        for(row = len; row > 0; row--)
        {
            for(col = 0; col < row; col++)
            {
            if(n+col <= len-2)
                printf("  ");
             
            for(k=0; k<=n; k++)
            {
                if((n+col > len-2) && (n+col <= len))
                if(middle+k > len-1)
                    printf("%c ",arr[(middle+k) - len]);
                else
                printf("%c ",arr[middle + k]);
            }
            }
            printf("\n");
            n++;
        }
    return 0;
}
