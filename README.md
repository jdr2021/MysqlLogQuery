# MysqlLogQuery
代码审计工具，用于监听mysql日志，支持mysql8.0以上和以下的版本。

# 支持的版本
目前8.0以上和以下版本，经过测试是可以正常使用的。

## Mysql 5.7.26版本
![v5.7.26](https://github.com/jdr2021/MysqlLogQuery/blob/master/864fb0821530a729bad18f5177407e4.png)

## Mysql 8.0.12版本
![v8.0.12](https://github.com/jdr2021/MysqlLogQuery/blob/master/c9e681e8023bd4e275d9bdd0a62e619.png)

# 已实现的功能

1. Mysql 8.0版本以上和8.0版本以下的日志都可监听。
2. 可删除指定行的日志数据，也可全部清除。
3. 可编辑任意SQL列的行内容，但不可修改。


# 使用方式

1. 运行jar包，双击或者java -jar *.jar
2. 在确保本地mysql数据库运行的情况下，点击连接，即可连接上mysql数据库。
3. 当执行sql语句后，点击更新，即可看见预期被执行的SQL。
4. 通过鼠标选择行数据后，点击清除，即可删除指定行的日志数据。

# 待解决的问题

脏数据过多，没有想到比较好的过滤方式，因此这里是用清除按钮，以人工方式过滤数据。

# 可能会存在的问题

日志监听的数据，可能没有自己预期执行的SQL。  
可在MainController.java文件的第102行修改limit的值，使用调试的方式，找到日志相关信息。
