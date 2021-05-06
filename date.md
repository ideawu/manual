Shell:

```
date "+%Y-%m-%d %H:%M:%S"
date "+%F %T"

# 显示时间戳
date "+%s"

# 解析时间戳(Linux)
date -d @1620289726 "+%Y-%m-%d %H:%M:%S"

# 解析时间戳(macOS)
date -r 1620289726 "+%Y-%m-%d %H:%M:%S"
```


PHP:

```
php -r "echo date('Y-m-d H:i:s');"
```
