```
tcpdump -i eth1 'port 80' -vv

tcpdump -i eth1 'port 80 and src 1.1.1.1' -vv

tcpdump 'src 1.1.1.1' -vv

tcpdump 'dst 1.1.1.1' -vv

tcpdump 'src port 80' -vv

-w a.txt 把报文内容写到文件中
```
