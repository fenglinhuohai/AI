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

例3 aabb问题，aabb是完全平方数，且具有aabb格式

```
#include<stdio.h>
#include<math.h>
int main(){
    for(int a = 1;a <= 9;a++){
        for(int b = 1;b <= 9;b++){
            int n = 1100 * a + 11 * b;
            // int m = floor(sqrt(n) + 0.5);
            int m = sqrt(n);
            if(n == m * m){
                printf("%d\n",n);
            }
        }
    }

    for(int i = 1;;i++){
        int n = i * i;
        if(n < 1000)
            continue;
        if(n > 9999)
            break;
        int ho = n / 100;
        int lo = n % 100;
        if(ho / 10 == ho % 10 && lo / 10 == lo % 10)
            printf("%d\n",n);
    }
    return 0;
}
```

例4 开灯问题，n盏灯，1～n，第一个人把所有灯打开，第二个人按下所有为2倍数的灯，第三个人按下所有3倍数的灯，一共k个人，问，最后哪些灯开着？

```
#include<stdio.h>
#include<string.h>
#define MAXN 1000
int lamp[MAXN];
int main(){
    int n,k;
    memset(lamp,0,sizeof(lamp));
    scanf("%d%d",&n,&k);
    for(int i = 1;i <= k;i++){
        for(int j = 1;j <= n;j++){
            if(j % i == 0)
                lamp[j] = !lamp[j];
        }
    }
    for(int i = 1;i <= n;i++)
        if(lamp[i])
            printf("%d ",i);
    printf("\n");
    return 0;
}
```





