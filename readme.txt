运行聊天室流程
安装erlang环境
1 将chat_server.erl  chat_send_client.erl chat_recv_client.erl 放在同一个目录 
2 输入erl进入命令行 
3 c("/path/").  #进入目录
4 c(chat_server). 
  c(chat_send_client).
  c(chat_recv_client).  #编译
5启动server
    chat_server:start(9999).
6启动client1 send端
    client1=chat_send_client:start("localhost",9999).
    另起一个窗口启动client1 recv端
    client11=chat_recv_client:start("localhost",9999).
7 如果启动多个客户端 重复操作6    

