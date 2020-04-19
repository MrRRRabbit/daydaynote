# daydaynote
记录每天技术研究的小发现
> 2022-02-20
1.  java集合的removeAll方法会移除入参中集合出现过的元素相同的所有元素，无数量限制
```
A=[1,2,2,3]
B=[2]
A.removeAll(B)后
A=[1,3]
```
> 2022-02-28
1.  java的Scanner.nextLine()函数会接收回车及空格及tab等特殊字符作为输入，在其它输入回车的输入操作之后试用，可能会出现跳过nextLine函数没执行的假象

>2022-03-10
1.  Spring注解@Controller需和注解@ResponseBody配合使用，建议用@RestController注解
2.  mapstruct框架使用时，target和source中有相同名称字段A和B，且B字段需映射C字段。请ignore字段A

>2022-03-11
1.  关于request请求中文乱码问题，需设置headers -> accept:*/*，同时需要请求客户端需设置MessageConverter支持MediaType.ALL
2.  服务端重定向，如果后面还有别的重定向逻辑，一定要return，否则会报以下异常
```
java.lang.IllegalStateException: Cannot call sendRedirect() after the response has been committed
```
>2022-03-25
1.  curl模拟get post请求
参数说明
-i 显示全部信息
-l 只显示头部信息
-v 显示get请求全过程解析
```
curl -H "Content-type: application/json" -X POST -d '{"key1":"value1"}' 服务地址
curl -d "param1=value1&param2=value2" 服务地址
```
2.  telnet 与远程服务建立连接
```
telnet 主机 端口
```
