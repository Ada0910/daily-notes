# grep命令
- 根据关键字查询日志
```
cat 1.log | grep key 可以写为： grep key 1.log
```

##  举例
- 假设存在日志文件 hrun.log，查询的关键字为”新增用户”：


根据关键字查看日志

 ```
 cat hrun.log | grep “新增用户” 
 ```

根据关键字查看后10行日志
 ```
 cat hrun.log | grep “新增用户” -A 10 
 ```

根据关键字查看前10行日志
 ```
 cat hrun.log | grep “新增用户” -B 10 
 ```

根据关键字查看前后10行日志，并显示出行号
 ```
 cat -n hrun.log | grep “新增用户” -C 10 
 ```

查看日志前 50 行
 ```
 cat hrun.log | head -n 50 
 ```

查看日志后 50 行，并显示出行号
 ```
 cat -n hrun.log | tail -n 50 
 ```

说明： 

```
-A 表示关键字之后，After
-B 表示关键字之前，Before
-C 表示关键字前后，Context
```