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





