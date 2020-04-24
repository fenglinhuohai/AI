1、C语言循环输入：

```
while(scanf("%d",&n) != EOF)
```

EOF:End of File，在studio.h文件中，定义为\#define EOF \(-1\)，scanf函数返回输入数字的个数，当输入为-1时，表示，输入结束

2、C语言的数据大小范围：![](https://img2018.cnblogs.com/blog/1764291/201908/1764291-20190809103400157-922796731.png)3、scanf输入：

返回输入个数，如果遇到文件末尾或者终止输入，会返回-1，即EOF

window下：ctrl+z结束输入，linux下：ctrl+d结束输入

