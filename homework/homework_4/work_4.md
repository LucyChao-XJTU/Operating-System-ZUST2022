1. 信号量 Sr的作用: 读者之间互斥访问rc变量，防止计数出现覆盖错误

   

2. 读写互斥：

   ①.if rc=1 then P(S); 有读者在读，不能进行写操作

   ②.if rc=0 then V(S); 没有读者在读，可以进行写操作

   ③.‌‌P(S); Write file; V(S); 写操作进行时，不能读。

3. 在读者程序内添加 if rc=5 then P(Sr);