1、C语言循环输入：

```
while(scanf("%d",&n) != EOF)
```

EOF:End of File，在studio.h文件中，定义为\#define EOF \(-1\)，scanf函数返回输入数字的个数，当输入为-1时，表示，输入结束

2、C语言的数据大小范围：![](https://img2018.cnblogs.com/blog/1764291/201908/1764291-20190809103400157-922796731.png)3、scanf输入：

返回输入个数，如果遇到文件末尾或者终止输入，会返回-1，即EOF

window下：ctrl+z结束输入，linux下：ctrl+d结束输入

4、文件输入输出、重定向输入输出框架：

```
#include<stdio.h>
#include<limits.h>
#define LOCAL
// 输入一些数字，求出这些数字的最小值，最大值，平均值。
int main(){
    #ifdef LOCAL
    freopen("data/rdata.in","r",stdin);
    freopen("data/rdata.out","w",stdout);
    #endif // LOCAL
    int a[1024],tmp;
    int max = INT_MIN,min = INT_MAX,n = 0;
    float sum = 0;
    while(scanf("%d",&tmp) == 1){
        a[n++] = tmp;
        sum += tmp;
        if(max < tmp)
            max = tmp;
        if(min > tmp)
            min = tmp;
    }
    printf("最小值:%d\n",min);
    printf("最大值:%d\n",max);
    printf("平均值:%.2f\n",sum / n);

    FILE *fin, *fout;
    fin = fopen("data/data.in","rb");
    fout = fopen("data/data.out","wb");
    max = INT_MIN,min = INT_MAX,n = 0;
    sum = 0;
    while(fscanf(fin,"%d",&tmp) == 1){
        sum += tmp;
        a[n++] = tmp;
        if(max < tmp)
            max = tmp;
        if(min > tmp)
            min = tmp;
    }
    fprintf(fout,"%d %d %.2f\n",min,max,sum / n);
    return 0;
}
```

5、c语言中getchar：

[https://blog.csdn.net/meidong52617/article/details/44728517](https://blog.csdn.net/meidong52617/article/details/44728517)



