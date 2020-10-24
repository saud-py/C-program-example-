#include<stdio.h>
#include<conio.h>
int a[100], n, ele, i, pos;
void create()
{
    printf("\nEnter the size of the array:");
    scanf("%d",&n);
    printf("\nEnter the elements for the array\n");
    for(i=0;i<n;i++)
        scanf("%d",&a[i]);
}
void display()
{
    int i;
    printf("\nThe array elements are:\n");
    for(i=0;i<n;i++)
    {
        printf("%d\t", a[i]);
    }
}
void insert()
{
    printf("\nEnter the position for the new elements: ");
    scanf("%d", &pos);
    printf("\nEnter the element to be inserted: ");
    scanf("%d", &ele);
    for(i=n-1; i>=pos; i--)
    {
        a[i+1] = a[i];
    }
    a[pos] = ele;
    {
        a[i+1] = a[i];
    }
    a[pos] = ele;
    n=n+1;
}
void del()
{
    printf("\nEnter the position of the element to be deleted:");
    scanf("%d", &pos);
    ele = a[pos];
    for(i=pos; i<n-1; i++)
    {
        a[i] = a[i+1];
    }
    n = n-1;
    printf("\n The deleted element is =%d", ele);
}

void main()
{

    int ch;

    do{
        printf("--------\n");
        printf("\n MENU: \n");
        printf("-------\n");
        printf("Choose an option:");
        printf("\t 1.Create \t 2.Display \t 3.Insert \t 4.Delete \t 5. Exit \n");
        printf("=======");
        printf("Enter your choice: ");
        scanf("%d", &ch);
        switch(ch)
        {
            case 1: create();
                    break;
            case 2: display();
                    break;
            case 3: insert();
                    break;
            case 4: del();
                    break;
            case 5: exit(0);
                    break;
            default: printf("\n Invalid Input: \n");
                    break;
        }
    }while(ch!=5);
    getch();
}
