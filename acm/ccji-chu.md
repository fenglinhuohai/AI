1、C语言循环输入：

```
while(scanf("%d",&n) != EOF)
```

EOF:End of File，在studio.h文件中，定义为\#define EOF \(-1\)，scanf函数返回输入数字的个数，当输入为-1时，表示，输入结束

2、C语言的数据大小范围：

char -128 ~ +127 \(1 Byte\)  
short -32768 ~ + 32767 \(2 Bytes\)  
unsigned short 0 ~ 65536 \(2 Bytes\)  
int -2147483648 ~ +2147483647 \(4 Bytes\)  
unsigned int 0 ~ 4294967295 \(4 Bytes\)  
long == int  
long long -9223372036854775808 ~ +9223372036854775807 \(8 Bytes\)  
double 1.7 \* 10^308 \(8 Bytes\)

unsigned int 0～4294967295   
long long的最大值：9223372036854775807  
long long的最小值：-9223372036854775808  
unsigned long long的最大值：18446744073709551615

\_\_int64的最大值：9223372036854775807  
\_\_int64的最小值：-9223372036854775808  
unsigned \_\_int64的最大值：18446744073709551615

