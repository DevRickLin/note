1. HTTP是指超文本传输协议
2. HTTP属于[应用层](应用层)协议
3. HTTP使用TCP作为其支称，其不关心数据丢失和亂序問題
4. HTTP屬於無狀態協議，其不保存任何關於客戶的信息(所以才需要cookie)
5. HTTP的请求报文格式为
```
METHOD URL VERSION\cr\lf
FIELDNAME VALUE\CR\lf
\cr\lf
entity
```
6. HTTP的响应格式为
```
VERSION CODE PHARASE\cr\lf
FIELDNAME VALUE\cr\lf
\cr\lf
entity
```