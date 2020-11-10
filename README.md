# -
介绍一下十种排序方法 以及我对于·这些排序方法的理解
# 十种排序方法
## 插入排序
```
#include<stdio.h>
int main(void)
{
    int a[11];
    for(int i=1;i<=10;i++)
        scanf("%d",&a[i]);
    for(int i=1;i<=9;i++)
        {
            int key=a[i+1];
            int j=i;
            while(j>0 && a[j]>key)
            {
                a[j+1]=a[j];
                j--;
            }
            a[j+1]=key;
        }
     for(int i=1;i<=10;i++)
        printf("%d ",a[i]);   
        return 0;
}
/* for(int i=2;i<=10;i++)
        {
            int key=a[i];
            int j=i-1;
            while(j>0 && a[j]>key)
            {
                a[j+1]=a[j];
                j--;
            }
            a[j+1]=key;
        }
*/
```
## 冒泡排序
```
#include<stdio.h>
int main(void)
{
    int a[11], key;
    for (int i = 1; i <= 10; i++)
        scanf_s("%d", &a[i]);
    for (int i = 10; i >1; i--)
        for (int j = 1; j < i; j++)
        {
            key = a[j];
            if (a[j + 1] <a[j])//此处还可以使用swap函数或者运用指针自定义函数。
            {
                a[j] = a[j + 1];
                a[j + 1] = key;
            }
        }
    for (int i = 1; i <= 10; i++)
        printf("%d ", a[i]);
    return 0;
} 

    
