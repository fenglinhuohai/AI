例1 三位数反转

```
#include<stdio.h>
int main(){
    int number;
    while(scanf("%d",&number) != EOF){
        printf("%d%d%d\n",number%10,number/10%10,number/100);
    }
    return 0;
}
```

例2 交换两数

```
#include<stdio.h>
int main(){
    int a,b;
    scanf("%d%d",&a,&b);
    // Method 1:
    int t = a;
    a = b;
    b = t;
    printf("%d %d\n",a,b);
    // Method 2:
    a = a + b;
    b = a - b;
    a = a - b;
    printf("%d %d\n",a,b);
    // Method 3:异或运算
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;
    printf("%d %d\n",a,b);
    return 0;
}
```





